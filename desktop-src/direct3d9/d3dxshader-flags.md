---
description: I flag D3DXSHADER vengono usati per l'analisi, la compilazione o l'assemblaggio di shader.
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: Flag D3DXSHADER (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_PACKMATRIX_COLUMNMAJOR
- D3DXSHADER_PACKMATRIX_ROWMAJOR
- D3DXSHADER_AVOID_FLOW_CONTROL
- D3DXSHADER_DEBUG
- D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_IEEE_STRICTNESS
- D3DXSHADER_NO_PRESHADER
- D3DXSHADER_OPTIMIZATION_LEVEL0
- D3DXSHADER_OPTIMIZATION_LEVEL1
- D3DXSHADER_OPTIMIZATION_LEVEL2
- D3DXSHADER_OPTIMIZATION_LEVEL3
- D3DXSHADER_PARTIALPRECISION
- D3DXSHADER_PREFER_FLOW_CONTROL
- D3DXSHADER_SKIPOPTIMIZATION
- D3DXSHADER_SKIPVALIDATION
- D3DXSHADER_USE_LEGACY_D3DX9_31_DLL
- D3DXSHADER_DEBUG
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_SKIPVALIDATION
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 031ae23301b78a9cced683551c9d7220aa66f7e0a48b504fe1a93721fd8d6a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849781"
---
# <a name="d3dxshader-flags"></a>Flag D3DXSHADER

I **flag D3DXSHADER** vengono usati per l'analisi, la compilazione o l'assemblaggio di shader.

**Flag del parser**

I flag di tempo di analisi vengono usati dal sistema degli effetti (prima della compilazione dell'effetto) solo quando si crea un compilatore di effetti. Ad esempio, è possibile creare un oggetto compilatore con **D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR** e quindi usarlo ripetutamente con flag del compilatore diversi per generare codice specializzato.



| Costante                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR**</dt> </dl> | A meno che non vengano specificate in modo esplicito, le matrici verranno imballate in ordine principale della colonna (ogni vettore sarà in una singola colonna) quando vengono passate a e dallo shader. Questa operazione è in genere più efficiente perché consente di eseguire la moltiplicazione di matrice vettoriale usando una serie di prodotti punto.<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ ROWMAJOR**</dt> </dl>          | A meno che non vengano specificate in modo esplicito, le matrici verranno imballate in ordine principale di riga (ogni vettore sarà in una singola riga) quando vengono passate a o dallo shader.<br/>                                                                                                                                        |



**Flag del compilatore**

Il compilatore HLSL DirectX 10 è ora il compilatore predefinito. Per [informazioni dettagliate, vedere Strumento di compilazione effetti.](../direct3dtools/fxc.md)

Nella tabella seguente sono elencati in dettaglio i flag disponibili in Direct3D 9 e Direct3D 10. Il valore del flag è l'opzione fxc equivalente.



| Costante/valore                                                                                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_ EVITARE \_ IL CONTROLLO DI \_ FLUSSO**</dt> <dt>/Gfa</dt> </dl>                                     | Si tratta di un suggerimento per il compilatore per evitare l'uso di istruzioni di controllo di flusso.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ DEBUG**</dt> <dt>/Zi</dt> </dl>                                                                               | Inserire il nome file di debug, i numeri di riga e le informazioni sul tipo e sui simboli durante la compilazione dello shader.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_ ABILITA \_ COMPATIBILITÀ \_ CON LE VERSIONI PRECEDENTI**</dt> <dt>/Gec</dt> </dl> | Compilare ps \_ 1 \_ x shader come ps \_ 2 \_ 0. Gli effetti che specificano ps 1 x targets verranno invece compilati nelle destinazioni ps 2 0 perché si tratta della versione minima dello shader supportata dalla versione del compilatore shader fornita con \_ \_ \_ \_ DirectX 10. Questo flag non ha alcun effetto se usato con destinazioni di compilazione di livello superiore.<br/> Direct3D 9 - no<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ PS \_ SOFTWARE \_ NOOPT**</dt> <dt>N/D</dt> </dl>                      | Forzare la compilazione del compilatore sulla successiva destinazione software più alta disponibile per i pixel shader. Questo flag attiva anche le ottimizzazioni e il debug.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ VS \_ SOFTWARE \_ NOOPT**</dt> <dt>N/D</dt> </dl>                      | Forzare la compilazione del compilatore sulla successiva destinazione software più alta disponibile per i vertex shader. Questo flag attiva anche le ottimizzazioni e il debug.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_ IEEE \_ STRICTNESS**</dt> <dt>/Gis</dt> </dl>                                               | Disabilitare le ottimizzazioni che possono far sì che l'output di un programma shader compilato differisca dall'output di un programma compilato con il compilatore shader DirectX 9 a causa di piccoli errori di precisione nella matematica a virgola mobile.<br/> Direct3D 9 - no<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_ NO \_ PRESHADER**</dt> <dt>/Op</dt> </dl>                                                         | Disabilita i preshader. Il compilatore non estrarrà espressioni statiche per la valutazione nella CPU host. Inoltre, il compilatore non genera espressioni durante la compilazione di funzioni autonome.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_ LIVELLO \_ DI OTTIMIZZAZIONE0**</dt> <dt>/O0</dt> </dl>                                    | Livello di ottimizzazione più basso. Può produrre codice più lento, ma lo farà più rapidamente. Questo può essere utile in un ciclo di sviluppo shader altamente iterativo.<br/> Direct3D 9 - no<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_ LIVELLO \_ DI OTTIMIZZAZIONE 1**</dt> <dt>/O1</dt> </dl>                                    | Secondo livello di ottimizzazione più basso.<br/> Direct3D 9 - no<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_ LIVELLO \_ DI OTTIMIZZAZIONE 2**</dt> <dt>/O2</dt> </dl>                                    | Secondo livello di ottimizzazione più alto.<br/> Direct3D 9 - no<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_ LIVELLO \_ DI OTTIMIZZAZIONE3**</dt> <dt>/O3</dt> </dl>                                    | Livello di ottimizzazione più alto. Produrrà il codice migliore possibile, ma potrebbe richiedere molto più tempo. Ciò sarà utile per le compilazioni finali di un'applicazione in cui le prestazioni sono il fattore più importante.<br/> Direct3D 9 - no<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_ PARTIALPRECISION**</dt> <dt>/Gpp</dt> </dl>                                             | Forzare l'esecuzione di tutti i calcoli nello shader risultante con precisione parziale. Ciò può comportare una valutazione più rapida degli shader in alcuni componenti hardware.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_ PREFER \_ FLOW \_ CONTROL**</dt> <dt>/Gfp</dt> </dl>                                  | Si tratta di un suggerimento che il compilatore preferisce usare le istruzioni di controllo di flusso.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_ SKIPOPTIMIZATION**</dt> <dt>/Od</dt> </dl>                                              | Indicare al compilatore di ignorare i passaggi di ottimizzazione durante la generazione del codice. A meno che non si stia tentando di isolare un problema nel codice e si sospetta il compilatore, l'uso di questa opzione non è consigliato.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> <dt>/Vd</dt> </dl>                                                    | Non convalidare il codice generato in base alle funzionalità e ai vincoli noti. Questa opzione è consigliata solo quando si compilano shader noti per il funzionamento, ovvero gli shader compilati in precedenza senza questa opzione. Gli shader vengono sempre convalidati dal runtime prima di essere impostati sul dispositivo.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - Sì<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_ USARE \_ LA DLL LEGACY \_ D3DX9 \_ 31 \_**</dt> <dt>/LD</dt> </dl>                     | Abilitare l'uso del compilatore HLSL Direct3D 9 originale. OCT2006 \_ d3dx9 \_ 31x86.cab o \_ OCT2006 \_ d3dx9 \_ 31x64.cab deve essere incluso come parte della \_ redist delle applicazioni. Questo flag è necessario per compilare gli shader ps \_ 1 \_ x senza usare il flag di innalzamento di livello a ps \_ 2 \_ 0. Se si specifica questo flag quando si ottiene [**un'interfaccia ID3DXEffectCompiler,**](id3dxeffectcompiler.md) le chiamate successive a [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) e [**CompileShader**](id3dxeffectcompiler--compileshader.md) tramite questo oggetto usano il compilatore legacy.<br/> Direct3D 9 - Sì<br/> Direct3D 10 - no<br/> |



**Flag dell'assembler**

I flag dell'assembler vengono usati dal sistema di effetti per ottimizzare il codice dell'assembly shader ed effetto.



| Costante                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ DEBUG**</dt> </dl>                                                          | Inserire il nome file di debug, i numeri di riga e le informazioni sul tipo e sui simboli durante la compilazione dello shader.<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ PS \_ SOFTWARE \_ NOOPT**</dt> </dl> | Forzare la compilazione del compilatore sulla successiva destinazione software più alta disponibile per i pixel shader. Questo flag attiva anche le ottimizzazioni e il debug.<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ VS \_ SOFTWARE \_ NOOPT**</dt> </dl> | Forzare la compilazione del compilatore sulla successiva destinazione software più alta disponibile per i vertex shader. Questo flag attiva anche le ottimizzazioni e il debug.<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> </dl>                               | Non convalidare il codice generato in base alle funzionalità e ai vincoli noti. Questa opzione è consigliata solo quando si compilano shader noti per il funzionamento, ovvero gli shader compilati in precedenza senza questa opzione. Gli shader vengono sempre convalidati dal runtime prima di essere impostati sul dispositivo.<br/> |



## <a name="remarks"></a>Commenti

Il sistema di effetti **userà i flag del parser** quando viene chiamato dalle funzioni seguenti:

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md)

Il sistema di effetti userà **i flag del compilatore** quando viene chiamato dalle funzioni seguenti:

-   [**D3DXCompileShader**](d3dxcompileshader.md) (o [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) o [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md))
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) (o [**CompileShader**](id3dxeffectcompiler--compileshader.md))

È anche possibile  usare flag del compilatore quando si crea un effetto chiamando [**D3DXCreateEffect**](d3dxcreateeffect.md) (o [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) o [**D3DXCreateEffectFromResource).**](d3dxcreateeffectfromresource.md)

-   Se si passa un file con estensione fx non ricompilato, il sistema degli effetti userà il parametro di input flag durante la compilazione.
-   Se si passa un effetto compilato, il sistema di effetti ignorerà i flag del compilatore perché non sono necessari per caricare l'effetto.

Il sistema di effetti userà **i flag dell'assembler** quando viene chiamato dalle funzioni seguenti:

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

L'applicazione **di flag del compilatore** **o di assembler** all'API non corretta avrà esito negativo nella convalida dello shader. Controllare il valore restituito dal codice di errore Direct3D dalla funzione con lo strumento di ricerca errori DirectX (DXErr.exe) per rilevare l'errore. È possibile ottenere DXErr.exe informazioni da DirectX SDK. Per informazioni su DirectX SDK, vedere [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
