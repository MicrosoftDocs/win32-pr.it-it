---
description: Informazioni parametri
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: Informazioni parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe38cc9197df3ae22bcd72b824da5887647bca9e9d6101e3833d482fa907052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050771"
---
# <a name="parameter-information"></a>Informazioni parametri

Il [**metodo IMediaParamInfo::GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) restituisce una [**struttura MP \_ PARAMINFO**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) che descrive un parametro. Questa struttura contiene le informazioni seguenti:

-   Il **membro mpType** indica il tipo di dati del valore del parametro. Per migliorare l'efficienza, tutti i parametri vengono implementati come valori a virgola mobile a 32 bit. [**\_ L'enumerazione TYPE mp**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) definisce se interpretare il valore come integer, valore a virgola mobile, booleano o enumerazione (serie di interi).
-   Il **membro mopCaps** indica le curve supportate da questo parametro. Se il tipo di dati è booleano o di enumerazione, l'unica curva che il parametro può supportare è "Jump".
-   I **membri mpdMinValue** **e mpdMaxValue** definiscono i valori minimo e massimo per questo parametro. Tutte le curve per questo parametro devono rientrare in questo intervallo.
-   Il **membro mpdNeutralValue** è il valore predefinito del parametro .
-   Il **membro szLabel** è il nome del parametro e **il membro szUnitText** è il nome dell'unità di misura per il parametro. Ad esempio, "Volume" e "Decibel" o "Frequency" e "kHz". Entrambe le stringhe sono in lingua inglese e non vengono mai localizzate. Il DMO può fornire versioni localizzate tramite il [**metodo IMediaParamInfo::GetParamText.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext)

Le informazioni per ogni parametro rimangono fisse per tutta la durata del DMO. Di conseguenza, il client può eseguire una query per ottenere queste informazioni una sola volta e quindi memorizzarla nella cache.

**Formati di ora**

Il client deve impostare un timestamp per i dati di input, in modo che il DMO possa calcolare i valori dei parametri corrispondenti. Per impostazione predefinita, i timestamp rappresentano unità di 100 nanosecondi, denominate anche *ora di riferimento.* Questa unità di tempo non è utile per ogni applicazione, pertanto un DMO può supportare altri formati di ora. I formati di ora sono identificati dal GUID.



| **GUID**              | Descrizione                   |
|-----------------------|-------------------------------|
| RIFERIMENTO ORA \_ \_ GUID | Tempo di riferimento                |
| GUID \_ TIME \_ MUSIC     | Nota parti per trimestre (PPQN) |
| ESEMPI \_ DI ORA \_ GUID   | Esempi al secondo            |



 

Terze parti sono invitate a definire i propri formati di ora in base alle esigenze. Tuttavia, tutti gli oggetti DMO devono supportare il tempo di riferimento. In questo modo viene fornita una baseline standard che tutti possono usare. Per determinare il numero di formati di ora supportati DMO, chiamare il [**metodo IMediaParamInfo::GetNumTimeFormats.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) Per enumerare i formati supportati, chiamare [**il metodo IMediaParamInfo::GetSupportedTimeFormat.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat)

Per impostare il formato dell'ora, chiamare [**IMediaParams::SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat). Questo metodo specifica il GUID del formato dell'ora e i *dati relativi* all'ora , ovvero il numero di unità per tick del clock. Ad esempio, se il formato dell'ora è samples al secondo e i dati relativi all'ora sono 32, un valore timestamp pari a 10 corrisponde a 320 campioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Parametri dei supporti](media-parameters.md)
</dt> </dl>

 

 



