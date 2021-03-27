---
title: Costanti D3DCOMPILE (D3DCompiler. h)
description: Le costanti D3DCOMPILE specificano la modalità di compilazione del codice HLSL da parte del compilatore.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234957"
---
# <a name="d3dcompile-constants"></a>Costanti D3DCOMPILE

Le costanti D3DCOMPILE specificano la modalità di compilazione del codice HLSL da parte del compilatore.

<dl> <dt>

<span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**\_Debug D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Indica al compilatore di inserire le informazioni relative al file di debug, alla riga, al tipo o al simbolo nel codice di output.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ ignorare la \_ convalida**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Indica al compilatore di non convalidare il codice generato in base alle funzionalità note e ai vincoli. È consigliabile usare questa costante solo con gli shader che sono stati compilati correttamente in precedenza. DirectX convalida sempre gli shader prima di impostarli su un dispositivo.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**Ottimizzazione di D3DCOMPILE \_ Skip \_**
</dt> <dd> <dl> <dt>

(1 << 2)
</dt> <dt>



Indica al compilatore di ignorare i passaggi di ottimizzazione durante la generazione del codice. Si consiglia di impostare questa costante solo a scopo di debug.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**\_ \_ \_ Riga principale della matrice di D3DCOMPILE Pack \_**
</dt> <dd> <dl> <dt>

(1 << 3)
</dt> <dt>



Indica al compilatore di comprimere le matrici in ordine di riga, in base all'input e all'output dello shader.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**\_ \_ Colonna matrice D3DCOMPILE \_ pack \_ principale**
</dt> <dd> <dl> <dt>

(1 << 4)
</dt> <dt>



Indica al compilatore di comprimere matrici in base all'ordine delle colonne in base all'input e all'output dello shader. Questo tipo di compressione è in genere più efficiente perché una serie di prodotti punto può quindi eseguire la moltiplicazione della matrice vettoriale.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Precisione parziale \_ D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 5)
</dt> <dt>



Indica al compilatore di eseguire tutti i calcoli con precisione parziale. Se si imposta questa costante, il codice compilato potrebbe essere eseguito più velocemente su hardware.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ vs \_ software \_ No \_ opt**
</dt> <dd> <dl> <dt>

(1 << 6)
</dt> <dt>



Indica al compilatore di compilare un vertex shader per il successivo profilo dello shader più alto. Questa costante disattiva il debug e le ottimizzazioni.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ Force \_ PS \_ software \_ No \_ opt**
</dt> <dd> <dl> <dt>

(1 << 7)
</dt> <dt>



Indica al compilatore di compilare un pixel shader per il successivo profilo dello shader più alto. Questa costante disattiva anche il debug e le ottimizzazioni.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ senza \_ preshader**
</dt> <dd> <dl> <dt>

(1 << 8)
</dt> <dt>



Indica al compilatore di disabilitare i preshader. Se si imposta questa costante, il compilatore non estrae l'espressione statica per la valutazione.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ evitare \_ il \_ controllo di flusso**
</dt> <dd> <dl> <dt>

(1 << 9)
</dt> <dt>



Indica al compilatore di non usare i costrutti di controllo del flusso laddove possibile.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ preferisce \_ il \_ controllo di flusso**
</dt> <dd> <dl> <dt>

(1 << 10)
</dt> <dt>



Indica al compilatore di usare i costrutti di controllo del flusso laddove possibile.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ Abilita la \_ rigidità**
</dt> <dd> <dl> <dt>

(1 << 11)
</dt> <dt>



Forza la compilazione strict, che potrebbe non consentire la sintassi legacy.

Per impostazione predefinita, il compilatore Disabilita la limitazione della sintassi deprecata.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ Abilita \_ compatibilità con le versioni precedenti \_**
</dt> <dd> <dl> <dt>

(1 << 12)
</dt> <dt>



Indica al compilatore di abilitare gli shader meno recenti da compilare fino a 5 \_ 0 destinazioni.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_ strictity**
</dt> <dd> <dl> <dt>

(1 << 13)
</dt> <dt>



Impone la compilazione di IEEE Strict.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**\_Ottimizzazione D3DCOMPILE \_ level0**
</dt> <dd> <dl> <dt>

(1 << 14)
</dt> <dt>



Indica al compilatore di utilizzare il livello di ottimizzazione più basso. Se si imposta questa costante, il compilatore potrebbe produrre codice più lento, ma produrrà il codice più rapidamente. Impostare questa costante quando si sviluppa lo shader in modo iterativo.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**\_Ottimizzazione D3DCOMPILE \_ Level1**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Indica al compilatore di utilizzare il secondo livello di ottimizzazione più basso.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**\_Ottimizzazione D3DCOMPILE \_ Level2**
</dt> <dd> <dl> <dt>

((1 << 14) \| (1 << 15))
</dt> <dt>



Indica al compilatore di utilizzare il secondo livello di ottimizzazione più elevato.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**\_Ottimizzazione D3DCOMPILE \_ Level3**
</dt> <dd> <dl> <dt>

(1 << 15)
</dt> <dt>



Indica al compilatore di usare il livello di ottimizzazione più elevato. Se si imposta questa costante, il compilatore produce il migliore codice possibile, ma può richiedere molto più tempo. Impostare questa costante per le compilazioni finali di un'applicazione quando le prestazioni sono il fattore più importante.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**Gli \_ avvisi di D3DCOMPILE \_ sono \_ errori**
</dt> <dd> <dl> <dt>

(1 << 18)
</dt> <dt>



Indica al compilatore di considerare tutti gli avvisi come errori durante la compilazione del codice dello shader. Si consiglia di usare questa costante per il nuovo codice dello shader, in modo che sia possibile risolvere tutti gli avvisi e ridurre il numero di difetti del codice di difficile individuazione.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**\_Alias delle risorse di D3DCOMPILE \_ \_**
</dt> <dd> <dl> <dt>

(1 << 19)
</dt> <dt>



Indica al compilatore di presumere che le visualizzazioni di accesso non ordinate (UAV) e le visualizzazioni delle risorse dello shader (SRVs) possano avere alias per cs \_ 5 \_ 0.

> [!Note]  
> Questa costante del compilatore è nuova a partire da D3dcompiler \_47.dll.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ Abilita \_ \_ tabelle descrittore senza limiti \_**
</dt> <dd> <dl> <dt>

(1 << 20)
</dt> <dt>



Indica al compilatore di abilitare le tabelle di descrittori non vincolate.

> [!Note]  
> Questa costante del compilatore è nuova a partire da D3dcompiler \_47.dll.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ tutte \_ le risorse \_ associato**
</dt> <dd> <dl> <dt>

(1 << 21)
</dt> <dt>



Indica al compilatore di verificare che tutte le risorse siano associate.

> [!Note]  
> Questa costante del compilatore è nuova a partire da D3dcompiler \_47.dll.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





