---
description: I flag D3DXSHADER vengono usati per l'analisi, la compilazione o il montaggio degli shader.
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: Flag D3DXSHADER (D3dx9shader. h)
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
ms.openlocfilehash: 6f5d35f8c3bdf556e188c2cab8ff2684449b226f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322478"
---
# <a name="d3dxshader-flags"></a>Flag D3DXSHADER

I flag **D3DXSHADER** vengono usati per l'analisi, la compilazione o il montaggio degli shader.

**Flag del parser**

I flag di tempo di analisi vengono usati solo dal sistema degli effetti (prima della compilazione dell'effetto) quando si crea un compilatore di effetti. Ad esempio, è possibile creare un oggetto compilatore con **D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR** e quindi usare ripetutamente tale oggetto compilatore con flag del compilatore diversi per generare codice specializzato.



| Costante                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR**</dt> </dl> | A meno che non venga specificato in modo esplicito, le matrici verranno compresse nell'ordine delle colonne (ogni vettore si troverà in una singola colonna) quando vengono passate a e dallo shader. Questa operazione è in genere più efficiente perché consente l'esecuzione di una moltiplicazione di matrice vettoriale con una serie di prodotti dot.<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ ROWMAJOR**</dt> </dl>          | A meno che non venga specificato in modo esplicito, le matrici verranno compresse in ordine di riga (ogni vettore si troverà in un'unica riga) quando viene passato a o dallo shader.<br/>                                                                                                                                        |



**Flag del compilatore**

Il compilatore DirectX 10 HLSL è ora il compilatore predefinito. Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .

La tabella seguente illustra in dettaglio i flag disponibili in Direct3D 9 e Direct3D 10. Il valore per il flag è l'opzione FXC equivalente.



| Costante/valore                                                                                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_ EVITARE \_ il \_ controllo di flusso**</dt> <dt>/GFA</dt> </dl>                                     | Si tratta di un suggerimento al compilatore per evitare di usare le istruzioni di controllo del flusso.<br/> Direct3D 9-Sì<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ DEBUG**</dt> <dt>/Zi</dt> </dl>                                                                               | Inserire il nome del file di debug, i numeri di riga e le informazioni sul tipo e sui simboli durante la compilazione dello shader.<br/> Direct3D 9-Sì<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_ Abilita \_ \_ compatibilità con le versioni precedenti**</dt> <dt>/GEC</dt> </dl> | Compilare PS \_ 1 \_ x shaders come PS \_ 2 \_ 0. Gli effetti che specificano le \_ destinazioni PS 1 \_ x vengono invece compilati in \_ base alle destinazioni PS 2 \_ 0, perché si tratta della versione minima dello shader supportata dalla versione del compilatore shader fornita con DirectX 10. Questo flag non ha effetto se usato con destinazioni di compilazione di livello superiore.<br/> Direct3D 9-No<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORZA \_ \_ \_ NOOPT software PS**</dt> <dt>N/A</dt> </dl>                      | Forza la compilazione del compilatore rispetto alla destinazione software più alta disponibile successiva per i pixel shader. Questo flag disattiva anche le ottimizzazioni e il debug in.<br/> Direct3D 9-Sì<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ vs \_ software \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | Forza la compilazione del compilatore rispetto alla destinazione software più alta disponibile successiva per i vertex shader. Questo flag disattiva anche le ottimizzazioni e il debug in.<br/> Direct3D 9-Sì<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_ /GIS di \_ rigidità IEEE**</dt> <dt></dt> </dl>                                               | Disabilitare le ottimizzazioni che potrebbero causare differenze tra l'output di un programma shader compilato e l'output di un programma compilato con il compilatore DirectX 9 shader a causa di errore di precisione ridotta nella matematica a virgola mobile.<br/> Direct3D 9-No<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_ Nessun \_ /op PREshader**</dt> <dt></dt> </dl>                                                         | Disabilita i preshader. Il compilatore non estrae le espressioni statiche per la valutazione sulla CPU dell'host. Inoltre, il compilatore non esegue il loft di espressioni durante la compilazione di funzioni autonome.<br/> Direct3D 9-Sì<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_ OTTIMIZZAZIONE \_ Level0**</dt> <dt>/o0</dt> </dl>                                    | Livello di ottimizzazione più basso. Può produrre codice più lento, ma sarà più rapido. Questa operazione può essere utile in un ciclo di sviluppo di shader altamente iterativo.<br/> Direct3D 9-No<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_ OTTIMIZZAZIONE \_ Level1**</dt> <dt>/O1</dt> </dl>                                    | Secondo livello di ottimizzazione più basso.<br/> Direct3D 9-No<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_ OTTIMIZZAZIONE \_ Level2**</dt> <dt>/O2</dt> </dl>                                    | Secondo livello di ottimizzazione più alto.<br/> Direct3D 9-No<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_ OTTIMIZZAZIONE \_ Level3**</dt> <dt>/O3</dt> </dl>                                    | Livello massimo di ottimizzazione. Produrrà il migliore codice possibile, ma potrebbe richiedere molto più tempo. Questa operazione sarà utile per le compilazioni finali di un'applicazione in cui le prestazioni sono il fattore più importante.<br/> Direct3D 9-No<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_**</dt> <dt>/GPP</dt> PARTIALPRECISION </dl>                                             | Forzare l'esecuzione di tutti i calcoli nello shader risultante a precisione parziale. Questo può comportare una valutazione più veloce degli shader in alcuni componenti hardware.<br/> Direct3D 9-Sì<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_ PREFERIRE \_ il \_ controllo di flusso**</dt> <dt>/GFP</dt> </dl>                                  | Si tratta di un suggerimento al compilatore che preferisce usare le istruzioni di controllo del flusso.<br/> Direct3D 9-Sì<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_**</dt> <dt>/Od</dt> SKIPOPTIMIZATION </dl>                                              | Indica al compilatore di ignorare i passaggi di ottimizzazione durante la generazione del codice. A meno che non si stia tentando di isolare un problema nel codice e si sospetta il compilatore, l'uso di questa opzione non è consigliato.<br/> Direct3D 9-Sì<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_**</dt> <dt>/VD</dt> SKIPVALIDATION </dl>                                                    | Non convalidare il codice generato in base alle funzionalità note e ai vincoli. Questa opzione è consigliata solo quando si compilano shader noti per funzionare, ovvero gli shader che hanno compilato prima senza questa opzione. Gli shader vengono sempre convalidati dal runtime prima che siano impostati sul dispositivo.<br/> Direct3D 9-Sì<br/> Direct3D 10-Sì<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_ USA \_ /LD \_ d3dx9 \_ 31 \_ dll legacy**</dt> <dt></dt> </dl>                     | Abilitare l'uso del compilatore HLSL Direct3D 9 originale. OCT2006 \_ d3dx9 \_ 31 \_x86.cab o OCT2006 \_ d3dx9 \_ 31 \_x64.cab deve essere incluso come parte delle applicazioni Redist. Questo flag è necessario per compilare \_ \_ gli shader PS 1 x senza usare il flag Promotion per PS \_ 2 \_ 0. Se si specifica questo flag quando si ottiene un'interfaccia [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , le chiamate successive a [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) e [**CompileShader**](id3dxeffectcompiler--compileshader.md) tramite questo oggetto utilizzeranno il compilatore legacy.<br/> Direct3D 9-Sì<br/> Direct3D 10-No<br/> |



**Flag assembler**

I flag dell'assembler vengono usati dal sistema di effetti per ottimizzare il codice dell'assembly dello shader e dell'effetto.



| Costante                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**\_Debug D3DXSHADER**</dt> </dl>                                                          | Inserire il nome del file di debug, i numeri di riga e le informazioni sul tipo e sui simboli durante la compilazione dello shader.<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ PS \_ software \_ NOOPT**</dt> </dl> | Forza la compilazione del compilatore rispetto alla destinazione software più alta disponibile successiva per i pixel shader. Questo flag disattiva anche le ottimizzazioni e il debug in.<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ vs \_ software \_ NOOPT**</dt> </dl> | Forza la compilazione del compilatore rispetto alla destinazione software più alta disponibile successiva per i vertex shader. Questo flag disattiva anche le ottimizzazioni e il debug in.<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**\_SKIPVALIDATION D3DXSHADER**</dt> </dl>                               | Non convalidare il codice generato in base alle funzionalità note e ai vincoli. Questa opzione è consigliata solo quando si compilano shader noti per funzionare, ovvero gli shader che hanno compilato prima senza questa opzione. Gli shader vengono sempre convalidati dal runtime prima che siano impostati sul dispositivo.<br/> |



## <a name="remarks"></a>Commenti

Il sistema degli effetti utilizzerà i **flag del parser** quando viene chiamato dalle funzioni seguenti:

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md)

Il sistema degli effetti utilizzerà i **flag del compilatore** quando viene chiamato dalle funzioni seguenti:

-   [**D3DXCompileShader**](d3dxcompileshader.md) (o [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) o [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md))
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) (o [**CompileShader**](id3dxeffectcompiler--compileshader.md))

Inoltre, è possibile usare i **flag del compilatore** quando si crea un effetto chiamando [**D3DXCreateEffect**](d3dxcreateeffect.md) (o [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) o [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)).

-   Se si passa un file con estensione FX non compilato, il sistema di effetti utilizzerà il parametro di input del flag durante la compilazione.
-   Se si passa un effetto compilato, il sistema di effetti ignorerà i flag del compilatore perché non sono necessari per caricare l'effetto.

Il sistema degli effetti utilizzerà i **flag dell'assembler** quando viene chiamato dalle funzioni seguenti:

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

L'applicazione dei flag **del compilatore** o dei **flag assembler** all'API non corretta non riuscirà a eseguire la convalida dello shader. Controllare il valore restituito del codice di errore Direct3D dalla funzione con lo strumento di ricerca degli errori di DirectX (DXErr.exe) per individuare l'errore. È possibile ottenere DXErr.exe e ottenere informazioni su di esso da DirectX SDK. Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
