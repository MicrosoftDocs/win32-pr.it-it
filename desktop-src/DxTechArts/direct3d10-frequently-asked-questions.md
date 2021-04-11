---
title: Domande frequenti su Direct3D 10
description: Questo articolo contiene alcune delle domande frequenti riguardanti Direct3D 10, dal punto di vista di uno sviluppatore che trasferisce un'applicazione esistente da Direct3D 9 (D3D9) a Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118007"
---
# <a name="direct3d-10-frequently-asked-questions"></a>Domande frequenti su Direct3D 10

Questo articolo contiene alcune delle domande frequenti riguardanti Direct3D 10, dal punto di vista di uno sviluppatore che trasferisce un'applicazione esistente da Direct3D 9 (D3D9) a Direct3D 10 (D3D10).

-   [Buffer costanti](#constant-buffers)
-   [State](#state)
-   [Formati](#formats)
-   [Collegamento shader](#shader-linkage)
-   [Chiamate di progetto](#draw-calls)
-   [Risorse](#resources)
-   [Profondità come trama](#depth-as-texture)
-   [MSAA](#msaa)
-   [Crashes](#crashes)
-   [Rendering predicato](#predicated-rendering)
-   [Geometry shader](#geometry-shader)
-   [HLSL](#hlsl)

## <a name="constant-buffers"></a>Buffer costanti

<dl> <dt>

<span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Qual è il modo migliore per aggiornare i buffer costanti?
</dt> <dd>

Il UpdateSubresource e la mappa con lo scarto dovrebbero avere una velocità pari alla stessa. Scegliere una delle due, a seconda di quale copia la quantità minima di memoria. Se i dati sono già archiviati in memoria in un blocco contiguo, usare UpdateSubresource. Se è necessario accumulare dati da altre posizioni, usare Map con scarto.

</dd> <dt>

<span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Qual è il modo peggiore per organizzare i buffer costanti?
</dt> <dd>

Le prestazioni peggiori vengono realizzate inserendo tutte le costanti per un particolare shader in un buffer costante. Sebbene questo sia spesso il modo più semplice per eseguire il porting da D3D9 a D3D10, può comportare un danneggiamento delle prestazioni. Si consideri ad esempio uno scenario in cui viene utilizzato il buffer costante seguente:

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

Il buffer è 6560 byte. Si supponga che esista un'applicazione con 1000 oggetti di cui eseguire il rendering, 100 di cui sono presenti mesh con skin e 900 di cui sono mesh statiche. Si supponga inoltre che l'applicazione utilizzi il mapping Shadow con una sorgente di luce. Ciò significa che sono disponibili due sessioni, una per la mappa di profondità sottoposta a rendering dalla luce e l'altra per il passaggio di rendering successivo. In questo modo vengono generate 2000 chiamate di progetto. Sebbene ogni chiamata di progetto non debba aggiornare ogni parte del buffer costante, l'intero buffer costante viene comunque aggiornato e inviato alla scheda. In questo modo si ottiene l'aggiornamento di 13 MB di dati ogni frame (2000 chiamate di chiamata volte a 6560 KB).

</dd> <dt>

<span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Qual è il modo migliore per organizzare i buffer costanti?
</dt> <dd>

Il modo migliore consiste nell'organizzare i buffer costanti in base alla frequenza di aggiornamento. Le costanti aggiornate a frequenze simili devono trovarsi nello stesso buffer. Si consideri, ad esempio, lo scenario presentato in "Qual è il modo peggiore per organizzare i buffer costanti?", ma con un layout costante migliore:

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

I buffer costanti vengono suddivisi in base alla frequenza di aggiornamento, ma questa è solo la metà della soluzione. L'applicazione deve aggiornare correttamente i buffer costanti per sfruttare al meglio la suddivisione. Si presuppone la stessa scena precedente: 900 mesh statiche, 100 mesh con skin, un passaggio di luce e un passaggio successivo. Si presuppone inoltre che vengano archiviati alcuni buffer costanti per ogni oggetto. Ciò significa che ogni oggetto conterrà un VSPerSkinnedCB o un VSPerStaticCB, a seconda che sia o meno una skin o statica. Questa operazione viene eseguita in modo da evitare il raddoppio della quantità di matrici inviate attraverso la pipeline.

Il frame viene suddiviso in tre fasi. La prima fase è l'inizio del frame e non prevede alcun rendering, ma solo aggiornamenti costanti.

<dl> <dt>

<span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Inizio frame**
</dt> <dd>

-   Aggiornare VSGlobalPerFrameCB per il tempo applicazione (4 byte)
-   Aggiornamento 100 VSPerSkinnedCB per gli oggetti con skinning 100 (640000 byte)
-   Aggiornare VSPerStaticCB per 900 oggetti statici (57600 byte)

Il passaggio successivo è la mappa Shadow. Si noti che l'unico buffer costante effettivamente aggiornato è VSPerPassCB. Tutti gli altri buffer costanti sono stati aggiornati durante il passaggio di inizio del frame. Sebbene sia ancora necessario associare questi buffer costanti, la quantità di informazioni passate alla scheda video è minima, perché i buffer sono già stati aggiornati.

</dd> <dt>

<span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Passaggio ombreggiatura**
</dt> <dd>

-   Aggiornare VSPerPassCB (72 byte)
-   Estrai mesh con skin 100 (100 associazioni, nessun aggiornamento)
-   Estrai 900 mesh statiche (100 associazioni, nessun aggiornamento)

Analogamente, il passaggio di rendering in diretta deve solo aggiornare i dati per materiale, perché non è stato archiviato per mesh. Se si presuppone che nella scena siano in uso materiali 500:

</dd> <dt>

<span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Passo successivo**
</dt> <dd>

-   Aggiornare VSPerPassCB (72 byte)
-   Aggiornamento 500 VSPerMaterialCBs (10000 byte)

Ciò comporta un totale di soli 707 KB. Sebbene si tratta di uno scenario molto semplice, viene illustrato il grado di riduzione del sovraccarico di aggiornamenti costanti mediante l'ordinamento delle costanti in base alla frequenza di aggiornamento.

</dd> </dl> </dd> <dt>

<span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>Cosa accade se non si dispone di spazio sufficiente per archiviare i singoli buffer costanti per le mesh, il materiale e così via? 
</dt> <dd>

È sempre possibile usare un sistema a più livelli di buffer costanti. Creare buffer costanti a dimensione variabile (16 byte, 32 byte, 64 byte e così via) fino alle dimensioni massime del buffer costante necessarie. Quando è il momento di associare un buffer costante a uno shader, selezionare il buffer costante più piccolo che può conservare i dati necessari per lo shader. Sebbene questo approccio sia leggermente meno efficiente, si tratta di un passaggio intermedio valido.

</dd> <dt>

<span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Si condividono buffer costanti tra diversi shader. Uno shader può usare tutte le costanti, ma un altro può usare alcune delle costanti. Qual è il modo migliore per aggiornarli? 
</dt> <dd>

Un approccio consiste nel suddividere ulteriormente il buffer costante. Tuttavia, viene visualizzato un punto in cui sono associati troppi buffer costanti. In questo caso, spostare le costanti che potrebbero essere inutilizzate da diversi shader alla fine del buffer costante. Quando si recuperano i dati della variabile dallo shader, usare il \_ flag D3D10 SVF \_ used dalla \_ variabile D3D10 shader \_ \_ DESC per determinare se la variabile viene usata. Inserendo le variabili inutilizzate alla fine del buffer costante, è possibile associare un buffer più piccolo allo shader che non usa queste variabili, risparmiando così il costo dell'aggiornamento.

</dd> <dt>

<span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Quanto è possibile migliorare la frequenza dei fotogrammi se si caricano solo le ossa dei miei caratteri una volta per ogni fotogramma anziché una volta per passaggio/estrazione? 
</dt> <dd>

È possibile migliorare la frequenza dei fotogrammi tra l'8% e il 50% a seconda della quantità di dati ridondanti. Nel peggiore dei casi, le prestazioni non verranno ridotte.

</dd> <dt>

<span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Quanti buffer costanti è necessario associare contemporaneamente? 
</dt> <dd>

Associare il numero minimo di buffer costanti necessari per ottenere tutti i dati nello shader. In uno scenario realistico, cinque è il numero consigliato di buffer costanti da usare. Anche la condivisione di buffer costanti tra gli shader (associazione dello stesso CB a VS e PS) può migliorare le prestazioni.

</dd> <dt>

<span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>È previsto un costo per l'associazione di buffer costanti senza utilizzarli? 
</dt> <dd>

Sì, se non si intende usare effettivamente il buffer, non chiamare VSSetConsantBuffer o PSSetConstantBuffer. Questo overhead dell'API aggiuntivo può essere aggiunto nel corso di più chiamate di estrazione.

</dd> </dl>

## <a name="state"></a>State

<dl> <dt>

<span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Qual è il modo migliore per gestire lo stato in D3D10? 
</dt> <dd>

La soluzione migliore consiste nel comprendere tutti gli Stati di prima e creare gli oggetti di stato in primo piano. Ciò significa che in fase di rendering, l'associazione di stato è l'unica operazione che deve essere eseguita. D3D10 filtra anche i duplicati.

</dd> <dt>

<span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Il gioco è stato caricato dinamicamente o contiene contenuto generato dall'utente. Non è possibile caricare tutti gli oggetti di stato in primo piano. Cosa devo fare? 
</dt> <dd>

Qui sono disponibili due soluzioni. Il primo consiste nel creare solo oggetti di stato in tempo reale e consentire a D3D10 di filtrare i duplicati. Questa operazione, tuttavia, non è consigliata per scenari con molte modifiche all'oggetto di stato per frame. Una soluzione migliore consiste nell'eseguire l'hashing degli oggetti di stato e creare un oggetto stato solo se non è possibile trovare un oggetto che soddisfa i requisiti nella tabella hash. Il motivo per cui si usa una tabella hash personalizzata è che un'applicazione può selezionare un hash rapido in base allo scenario di utilizzo specifico dell'applicazione. Se, ad esempio, un'applicazione modifica solo rendertargetwritemask in BlendState e mantiene tutti gli altri valori uguali, l'applicazione può generare un hash da rendertargetwritemask anziché l'intera struttura.

</dd> <dt>

<span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>Lo stato di AlphaTest è Gone. Dove è andato? 
</dt> <dd>

AlphaTest dovrebbe ora essere prestazioni nello shader. Vedere l'esempio FixedFuncEMU.

</dd> <dt>

<span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>Cosa è successo ai piani di ritaglio utente? 
</dt> <dd>

I piani di ritaglio utente sono stati spostati nello shader. Esistono due modi per gestire questo problema. Il primo consiste nell'output SV \_ Clipdistance dal vertex shader o dalla geometria shader. L'altra opzione consiste nell'usare lo scarto nell'pixel shader in base a un valore passato dal vertex shader o dal geometry shader. Sperimentare entrambi per vedere quale è più veloce per uno scenario specifico. Se si usa SV \_ CLIPDISTANCE, l'hardware può usare una routine di ritaglio basata sulla geometria che può causare un rallentamento delle chiamate di tracciato con binding di geometria. Allo stesso modo, l'uso di discard sposta il lavoro al pixel shader, che può causare un'esecuzione più lenta delle chiamate di disegni con associazione a pixel.

</dd> <dt>

<span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>I cancellamenti non rispettano le impostazioni dello stato, ad esempio le impostazioni del recto della forbice nello stato di rasterizzazione. 
</dt> <dd>

Le cancellazioni sono state separate dallo stato della pipeline. Per ottenere un comportamento di tipo D3D9, emulare i cancellamenti disegnando un quad a schermo intero.

</dd> <dt>

<span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Ho impostato di nuovo gli Stati su predefinito per provare a diagnosticare un errore di rendering. Ora la schermata mostra semplicemente il nero, anche se so che sto disegnando oggetti sullo schermo. 
</dt> <dd>

Quando si imposta stato di nuovo su valori predefiniti (NULL), assicurarsi che SampleMask nella chiamata a OMSetBlendState non sia mai zero. Se SampleMask è impostato su zero, tutti gli esempi vengono logicamente e con zero. In questo scenario nessun campione supererà il test di Blend.

</dd> <dt>

<span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Dove si è D3DSAMP lo \_ stato SRGBTEXTURE? 
</dt> <dd>

SRGB è stato rimosso come parte dello stato del campionatore ed è ora associato al formato di trama. Il binding di una trama SRGB comporterà lo stesso campionamento che si otterrebbe se è stato specificato D3DSAMP \_ SRGBTEXTURE in Direct3D 9.

</dd> </dl>

## <a name="formats"></a>Formati

<dl> <dt>

<span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Quale formato D3D9 corrisponde al formato D3D10? 
</dt> <dd>

Per informazioni, vedere [considerazioni su Direct3D 9 in Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

</dd> <dt>

<span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>Che cosa è successo ai formati di trama A8R8G8B8? 
</dt> <dd>

Sono stati deprecati in D3D10. È possibile ricreare le trame come R8G8B8A8 oppure swizzle durante il caricamento oppure è possibile swizzle nello shader.

</dd> <dt>

<span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Ricerca per categorie usare le trame pallettizzati? 
</dt> <dd>

Posizionare la tavolozza dei colori in una trama o in un buffer costante e associarla alla pipeline. Nella pixel shader eseguire una ricerca indiretta usando l'indice nella trama pallettizzati.

</dd> <dt>

<span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Quali sono i nuovi formati SRGB? 
</dt> <dd>

SRGB è stato rimosso come parte dello stato del campionatore ed è ora associato al formato di trama. Il binding di una trama SRGB comporterà lo stesso campionamento che si otterrebbe se è stato specificato D3DSAMP \_ SRGBTEXTURE in Direct3D 9.

</dd> <dt>

<span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Dove sono andate le ventole del triangolo? 
</dt> <dd>

Le ventole del triangolo sono state deprecate in D3D10. Le ventole del triangolo dovranno essere convertite nella pipeline del contenuto o in caso di caricamento.

</dd> </dl>

## <a name="shader-linkage"></a>Collegamento shader

<dl> <dt>

<span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Gli shader Direct3D 9 vengono compilati correttamente nel modello di Shader 4,0, ma quando vengono associati alla pipeline, si ottengono errori di collegamento visualizzati nell'output di debug con il runtime di debug. 
</dt> <dd>

Il collegamento dello shader è molto più restrittivo in D3D10. Gli elementi in una fase successiva devono essere letti nell'ordine in cui sono restituiti dalla fase precedente. Ad esempio:

Un vertex shader restituisce:

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

Pixel shader letture:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

Sebbene la posizione non sia necessaria nell'pixel shader, questo genera un errore di collegamento, perché la posizione viene restituita dal vertex shader, ma non letta dall'pixel shader. La versione più corretta avrà un aspetto simile al seguente:

Un vertex shader restituisce:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

Pixel shader letture:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

In questo caso, il vertex shader sta inserendo le stesse informazioni, ma ora il pixel shader legge elementi nell'output dell'ordine. Poiché il pixel shader non legge nulla dopo Tex, non è necessario preoccuparsi del fatto che Visual Studio consentirà di ottenere altre informazioni rispetto a quelle eseguite da PS.

</dd> <dt>

<span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Per creare un layout di input è necessario disporre di una firma shader, ma caricare le mesh e creare i layout prima di creare shader. Cosa devo fare? 
</dt> <dd>

Una soluzione consiste nel modificare l'ordine e caricare gli shader prima di caricare mesh. Tuttavia, questa operazione è molto più semplice di quanto detto. È sempre possibile creare il layout di input su richiesta quando necessario per l'applicazione. È necessario che sia presente una versione della firma dello shader. È necessario creare un hash basato sullo shader e sul layout del buffer e creare solo il layout di input se non esiste già un valore che corrisponde a.

</dd> </dl>

## <a name="draw-calls"></a>Chiamate di progetto

<dl> <dt>

<span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Qual è il limite per le chiamate di progetto che D3D10 può raggiungere 60 Hz? 30 Hz? 
</dt> <dd>

Direct3D 9 ha avuto una limitazione per il numero di chiamate di progetto a causa del costo della CPU per ogni chiamata di progetto. In Direct3D 10, il costo di ogni chiamata di estrazione è stato ridotto. Tuttavia, non esiste più una correlazione definita tra le chiamate di estrazione e la frequenza di fotogrammi. Poiché le chiamate di estrazione spesso richiedono molte chiamate di supporto (aggiornamenti costanti del buffer, binding di trama, impostazione dello stato e così via), l'effetto della frequenza dei fotogrammi dell'API è ora più dipendente dall'utilizzo complessivo delle API anziché semplicemente da un numero elevato di chiamate.

</dd> </dl>

## <a name="resources"></a>Risorse

<dl> <dt>

<span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Quale tipo di utilizzo delle risorse è consigliabile utilizzare per le operazioni? 
</dt> <dd>

Usare il foglio informativo seguente:

-   La CPU aggiorna la risorsa più di una volta per fotogramma: utilizzo di D3D10 \_ \_ dinamico
-   La CPU aggiorna la risorsa meno di una volta per frame: D3D10 \_ Usage \_ default
-   La CPU non aggiorna la risorsa: l'utilizzo di D3D10 non è \_ \_ modificabile
-   La CPU deve leggere la risorsa: \_ gestione temporanea dell'utilizzo di D3D10 \_

Poiché i buffer costanti sono sempre destinati a essere aggiornati di frequente, non sono conformi al "Cheat-Sheet". Per i tipi di risorse da usare per i buffer costanti, vedere la sezione [buffer costanti](#constant-buffers) .

</dd> <dt>

<span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>Cosa è successo a DrawPrimitiveUP e DrawIndexedPrimitiveUP? 
</dt> <dd>

Sono andati a D3D10. Per la geometria dinamica usare un buffer dinamico di utilizzo D3D10 di grandi dimensioni \_ \_ . All'inizio del frame, eseguirne il mapping con D3D10 \_ Map \_ Write \_ Ignora. Per ogni chiamata di disegno successiva, avanzare il puntatore di scrittura oltre la posizione dei vertici disegnati in precedenza ed eseguire il mapping del buffer con D3D10 \_ Map \_ Write no overwrite \_ \_ . Se si avvicina la fine del buffer prima della fine del frame, eseguire il wrapping del puntatore di scrittura intorno all'inizio ed eseguire il mapping con lo \_ scarto di scrittura della mappa D3D10 \_ \_ .

</dd> <dt>

<span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>È possibile scrivere indici a 16 bit e indici a 32 bit nello stesso buffer di geometria dinamica? 
</dt> <dd>

Sì, è possibile, ma ciò può comportare una riduzione delle prestazioni su determinati componenti hardware. È più sicuro creare buffer distinti per i dati di indice dinamici a 16 bit e i dati dell'indice a 32 bit.

</dd> <dt>

<span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Ricerca per categorie leggere i dati dalla GPU alla CPU? 
</dt> <dd>

È necessario utilizzare una risorsa di staging. Copiare i dati dalla risorsa GPU alla risorsa di gestione temporanea usando CopyResource. Eseguire il mapping della risorsa di gestione temporanea per leggere i dati.

</dd> <dt>

<span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>L'applicazione dipende dalla funzionalità StretchRect. 
</dt> <dd>

Poiché si trattava essenzialmente di un wrapper per la funzionalità Direct3D di base, è stato rimosso dall'API. Alcune delle funzionalità di StretchRect sono state spostate in D3DX10LoadTextureFromTexture. Per le conversioni di formato e la copia di trame, D3DX10LoadTextureFromTexture potrebbe eseguire il processo. Tuttavia, le operazioni, ad esempio la conversione da una dimensione a un'altra, possono richiedere un'operazione di rendering per la trama nell'applicazione.

</dd> <dt>

<span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Non ci sono offset o dimensioni nelle chiamate di mappa per le risorse. Queste erano presenti in caso di chiamate di blocco su Direct3D 9; perché sono cambiate? 
</dt> <dd>

Gli offset e le dimensioni delle chiamate di blocco in Direct3D 9 erano fondamentalmente disordine dell'API e spesso ignorati dal driver. Gli offset devono essere calcolati in alternativa dall'applicazione dal puntatore restituito nella chiamata della mappa.

</dd> </dl>

## <a name="depth-as-texture"></a>Profondità come trama

<dl> <dt>

<span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Che è più veloce? Se si usa la profondità come trama o si scrive la profondità in alfa e la si legge? 
</dt> <dd>

Si tratta di un'applicazione e di un hardware specifico. Usare quello che consente di risparmiare la larghezza di banda. Se si usano già più destinazioni di rendering e si ha un canale aggiuntivo, la scrittura della profondità dallo shader può essere una soluzione migliore. Inoltre, la scrittura di profondità in alfa o un'altra destinazione di rendering consente di scrivere valori di profondità lineare che potrebbero velocizzare i calcoli che devono accedere al buffer di profondità.

</dd> <dt>

<span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>È possibile fare in modo che una trama venga associata come input e associata come trama di stencil profondità purché si disabilitano le scritture di profondità? 
</dt> <dd>

Non in D3D10.

</dd> </dl>

## <a name="msaa"></a>MSAA

<dl> <dt>

<span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>È possibile risolvere una trama MSAA depth-stencil? 
</dt> <dd>

Non in D3D10. È tuttavia possibile campionare singoli campioni dalla trama MSAA. Per informazioni dettagliate, vedere la sezione [HLSL](#hlsl) .

</dd> <dt>

<span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Perché l'applicazione si arresta in modo anomalo non appena si Abilita MSAA? 
</dt> <dd>

Assicurarsi di abilitare un numero di campioni MSAA e un numero di qualità che vengono effettivamente enumerati dal driver.

</dd> </dl>

## <a name="crashes"></a>Crashes

<dl> <dt>

<span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>L'applicazione si arresta in modo anomalo in D3D10 o nel driver e non so perché. 
</dt> <dd>

Il primo passaggio consiste nell'abilitare il runtime di debug (il flag di [**debug di D3D10 \_ Create \_ Device \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) è stato passato in [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). Questa operazione esporrà gli errori più comuni come output di debug.

</dd> <dt>

<span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX si arresta in modo anomalo quando si tenta di utilizzare l'applicazione. 
</dt> <dd>

Il primo passaggio consiste nell'abilitare il runtime di debug (il flag di [**debug di D3D10 \_ Create \_ Device \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) è stato passato in [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). La probabilità di arresto anomalo di PIX è molto più elevata se l'output di debug non è pulito.

</dd> <dt>

<span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Il gioco esaurisce lo spazio degli indirizzi virtuali in vista a 32 bit in D3D10. Non sono presenti problemi in D3D9. 
</dt> <dd>

Si sono verificati alcuni problemi con D3D10 e lo spazio degli indirizzi virtuali. Questo problema è stato risolto in [KB940105](https://support.microsoft.com/kb/940105). Se il problema persiste, assicurarsi che non si stiano creando più risorse che possono essere mappate (bloccate) in D3D10 di quelle create in D3D9. Si pensi anche al porting a 64 bit, perché questo diventerà più diffuso in futuro.

</dd> </dl>

## <a name="predicated-rendering"></a>Rendering predicato

<dl> <dt>

<span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>Ho usato il rendering predicato (in base ai risultati delle query di occlusione). Perché l'app ha ancora la stessa velocità? 
</dt> <dd>

Prima di tutto, assicurarsi che il rendering che si desidera ignorare sia in realtà il collo di bottiglia dell'applicazione. Se non si tratta di un collo di bottiglia, il rendering non consentirà la frequenza dei fotogrammi.

In secondo luogo, assicurarsi che sia passato tempo sufficiente tra il problema della query e il rendering che si desidera predicare. Se la query non è stata completata nel momento in cui la chiamata di rendering raggiunge la GPU, il rendering si verificherà comunque.

In terzo luogo, predicazione Ignora solo determinate chiamate. Le chiamate ignorate sono di estrazione, cancellazione, copia, aggiornamento, ResolveSubresource e GenerateMips. L'impostazione dello stato, le chiamate di installazione, mapping e creazione di IA non rispettano predicazione. Se è presente una grande quantità di impostazioni di stato che consentono di predicare la chiamata di progetto, questi stati verranno comunque impostati.

</dd> </dl>

## <a name="geometry-shader"></a>Geometry shader

<dl> <dt>

<span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Devo usare geometry shader per conteggiarla suddividerla My (inserire qui)? 
</dt> <dd>

No. Il geometry shader non deve essere usato per lo schema a mosaico.

</dd> <dt>

<span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>È possibile usare geometry shader per creare la geometria? 
</dt> <dd>

Sì, in scenari molto limitati. Il geometry shader nelle parti D3D10 (2008) correnti non è equipaggiato per gestire una quantità eccessiva di espansione. Questo potrebbe cambiare in futuro. I fornitori di schede video possono avere un percorso speciale da una a quattro espansioni a causa dell'hardware punto-sprite esistente. Qualsiasi altra espansione dovrebbe essere molto limitata. Gli esempi di ParticlesGS e PipesGS raggiungono frequenze di frame elevate solo eseguendo un'espansione limitata. Vengono espansi solo pochi punti per fotogramma.

</dd> <dt>

<span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>Per cosa si deve usare geometry shader? 
</dt> <dd>

Qualsiasi elemento che richiede operazioni su un'intera primitiva, ad esempio il rilevamento della siluetta, le coordinate baricentrica e così via. Usarlo anche per selezionare la sezione di una matrice di destinazione di rendering a cui inviare le primitive.

</dd> <dt>

<span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>È possibile generare una quantità variabile di geometria dalla geometria shader? 
</dt> <dd>

Sì, ma ciò può causare problemi di prestazioni. Eseguire l'esempio di output di 1 punto per una chiamata e di 4 punti per un altro. Quando si adattano alle linee guida di espansione, è possibile che i thread geometry shader vengano eseguiti in modo seriale.

</dd> <dt>

<span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>In che modo D3D10 sa come generare indici adiacenza per la mesh? In alternativa, perché D3D10 non esegue correttamente il rendering quando si specifica che geometry shader necessita di informazioni adiacenza. 
</dt> <dd>

Le informazioni adiacenza non vengono create da D3D10, ma dall'applicazione. Gli indici adiacenza vengono generati dall'applicazione e devono contenere sei indici per primitiva; tra i sei, gli indici numerati dispari sono i vertici adiacenti dei bordi. ID3DX10Mesh:: GenerateAdjacencyAndPointsReps può essere usato per generare questi dati.

</dd> </dl>

## <a name="hlsl"></a>HLSL

<dl> <dt>

<span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Le istruzioni Integer e bit per bit sono lente? 
</dt> <dd>

Possono essere. Diverse schede D3D10 possono essere in grado di emettere solo operazioni integer su un subset delle unità ALU disponibili. Questo dipende molto dall'hardware. Vedere il singolo fornitore di hardware per indicazioni su come risolvere le operazioni integer su tale hardware specifico. Inoltre, prestare molta attenzione ai cast tra i tipi.

</dd> <dt>

<span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>Che cosa è successo a VPOS? 
</dt> <dd>

Se si dichiara un input per il pixel shader come \_ posizione SV, si otterrà lo stesso comportamento della dichiarazione come vPOS.

</dd> <dt>

<span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Ricerca per categorie campione di una trama MSAA? 
</dt> <dd>

Nello shader dichiarare la trama come Texture2DMS. È quindi possibile recuperare singoli esempi utilizzando i metodi di esempio all'esterno dell'oggetto Texture2DMS.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Ricerca per categorie indicare se viene effettivamente utilizzata una variabile shader in un buffer costante? 
</dt> <dd>

Esaminare lo struct D3D10 della \_ variabile shader \_ reflection \_ per la variabile. per uFlags deve essere \_ impostato il flag D3D10 SVF \_ used.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Ricerca per categorie indicare se una variabile shader in un buffer costante sta effettivamente utilizzando FX10? 
</dt> <dd>

Attualmente non è possibile usare FX10.

</dd> <dt>

<span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>Non ho alcun controllo sui buffer costanti creati da FX10. Come vengono creati e aggiornati? 
</dt> <dd>

Tutti i buffer costanti gestiti da FX10 vengono creati come \_ risorse predefinite di utilizzo di D3D10 \_ e vengono aggiornati con UpdateSubresource. Poiché FX10 mantiene un archivio di backup di tutti i dati costanti, UpdateSubresource è l'approccio migliore per aggiornarli.

</dd> <dt>

<span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Ricerca per categorie emulare la pipeline della funzione fissa usando gli shader? 
</dt> <dd>

Vedere l'esempio FixedFuncEMU.

</dd> <dt>

<span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>È consigliabile usare gli \[ hint del compilatore New unroll \] , \[ loop \] , \[ Branch \] e così via? 
</dt> <dd>

Generalmente, no. Il compilatore tenterà spesso entrambe le modalità e sceglierà quella più veloce. In alcuni casi, potrebbe essere necessario utilizzare l'operazione di \[ disrolling \] , ad esempio quando un recupero di trama all'interno di un ciclo deve accedere a una sfumatura.

</dd> <dt>

<span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>La precisione parziale fa qualsiasi differenza in D3D10? Posso specificare la precisione parziale nel HLSL di D3D9, ma non in D3D10 HLSL. 
</dt> <dd>

Tutte le operazioni di D3D10 vengono specificate per l'esecuzione in corrispondenza della precisione a virgola mobile a 32 bit. Pertanto, la precisione parziale non deve apportare alcuna differenza in D3D10.

</dd> <dt>

<span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In D3D9 è possibile eseguire il filtro delle ombreggiature HW PCF associando un buffer di profondità come trama e usando le normali istruzioni HLSL tex2D. Ricerca per categorie eseguire questa operazione in D3D10? 
</dt> <dd>

È necessario usare uno stato del campionatore di confronto e usare le istruzioni SampleCmp.

</dd> <dt>

<span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>In che modo questa parola chiave register funziona in D3D10? 
</dt> <dd>

La parola chiave register in D3D10 si applica ora a quale slot a cui è associata una determinata risorsa. In questo caso, la risorsa può essere un buffer (costante o altro), una trama o un campionatore.

-   Per i buffer costanti, usare la sintassi: Register (bN), dove N è lo slot di input (0-15)
-   Per le trame, usare la sintassi: Register (tN), dove N è lo slot di input (0-127)
-   Per i sampler, usare la sintassi: Register (sN), dove N è lo slot di input (0-127)

</dd> <dt>

<span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Ricerca per categorie inserire una variabile all'interno di un buffer costante se Register viene usato solo per specificare dove associare l'intero buffer? 
</dt> <dd>

Usare la parola chiave packoffset. L'argomento di packoffset è nel formato c \[ 0-4095 \] . \[ x, y, z, w \] . Ad esempio:

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

In questo buffer costante, IWaste2Floats viene inserito al terzo valore float (12 byte) nel buffer costante. IWasteMore viene inserito in corrispondenza del tredicesimo float4 o 52 float nel buffer costante.

</dd> </dl>

 

 