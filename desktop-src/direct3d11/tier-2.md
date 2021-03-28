---
title: Livello 2
description: In questa sezione viene descritto il supporto di livello 2.
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fa6e8ff3dba5780e3507bb2da5273e327a30e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872722"
---
# <a name="tier-2"></a>Livello 2

In questa sezione viene descritto il supporto di livello 2.

-   Hardware a livello di funzionalità minimo 11,1.
-   Tutte le funzionalità del livello precedente (senza limitazioni specifiche di [livello 1](tier-1.md) ) più le aggiunte nei seguenti elementi:
-   Sono disponibili le istruzioni dello shader per la compressione di LOD e il feedback dello stato mappato. Per altre informazioni, vedere [esposizione di risorse affiancate HLSL](hlsl-tiled-resources-exposure.md).
-   Letture da riquadri non mappati restituisce 0 in tutti i componenti non mancanti del formato e il valore predefinito per i componenti mancanti.
-   Le scritture nei riquadri non mappati vengono interrotte dalla memoria, ma potrebbero essere memorizzate nella cache che le letture successive allo stesso indirizzo potrebbero non essere rilevate.
-   Il filtraggio delle trame con un footprint che occupa riquadri **null** e non **null** contribuisce a 0 (con i valori predefiniti per i componenti di formato mancanti) per i Texel sui riquadri **null** nell'operazione di filtro complessiva. Alcuni componenti hardware iniziali non soddisfano questo requisito e restituisce 0 (con i valori predefiniti per i componenti di formato mancanti) per il risultato del filtro completo se eventuali Texel (con peso diverso da zero) rientrino in una sezione **null** . Nessun altro hardware potrà perdere la necessità di includere tutti i Texel (diversi da zero ponderati) nell'operazione di filtro.
-   Gli accessi a Texel **null** comportano l'operazione [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) sul feedback dello stato per una trama letta per restituire false. Indipendentemente dal modo in cui il risultato dell'accesso alla trama potrebbe essere mascherato nello shader e il numero di componenti presenti nel formato trama (la combinazione di che potrebbe far sembrare che non sia necessario accedere alla trama).
-   Vincoli di allineamento per le forme standard del riquadro: mipmap che riempiono almeno un riquadro standard in tutte le dimensioni è garantito l'uso dell'affiancamento standard, con il resto considerato compresso come **unità** in N riquadri (n segnalato all'applicazione). L'applicazione può eseguire il mapping dei riquadri N in posizioni arbitrariamente non contigue in un pool di sezioni, ma deve eseguire il mapping di tutti i riquadri compressi o di nessuno di essi. La compressione MIP è un set univoco di riquadri compressi per ogni sezione di matrice.
-   Sono supportati i filtri di riduzione min/max. Per informazioni sul filtro di riduzione min/max, vedere [funzionalità di campionamento delle trame delle risorse affiancate](tiled-resources-texture-sampling-features.md).
-   Le risorse affiancate con qualsiasi mipmap inferiore alle dimensioni del riquadro standard in qualsiasi dimensione non possono avere una dimensione della matrice maggiore di 1.
-   Limitazioni relative al modo in cui è possibile accedere ai riquadri quando sono presenti mapping duplicati, descritti in limitazioni di accesso ai riquadri [con mapping duplicati](tile-access-limitations-with-duplicate-mappings-.md), continuare con l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli di funzionalità delle risorse affiancate](tiled-resources-features-tiers.md)
</dt> </dl>

 

 