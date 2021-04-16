---
description: Informazioni parametri
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: Informazioni parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a311bbaa7907af0b3578ed88c28e573649f43
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522186"
---
# <a name="parameter-information"></a>Informazioni parametri

Il metodo [**IMediaParamInfo:: GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) restituisce una struttura [**MP \_ PARAMINFO**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) che descrive un parametro. Questa struttura contiene le informazioni seguenti:

-   Il membro **mpType** indica il tipo di dati del valore del parametro. Per maggiore efficienza, tutti i parametri sono implementati come valori a virgola mobile a 32 bit. L'enumerazione del [**\_ tipo MP**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) definisce se interpretare il valore come Integer, valore a virgola mobile, booleano o enumerazione (serie Integer).
-   Il membro **mopCaps** indica le curve supportate da questo parametro. Se il tipo di dati è booleano o Enumeration, l'unica curva che il parametro può supportare è "Jump".
-   I membri **mpdMinValue** e **mpdMaxValue** definiscono i valori minimo e massimo per questo parametro. Qualsiasi curva per questo parametro deve rientrare in questo intervallo.
-   Il membro **mpdNeutralValue** è il valore predefinito del parametro.
-   Il membro **szLabel** è il nome del parametro e il membro **szUnitText** è il nome dell'unità di misura per il parametro. Gli esempi possono includere "volume" e "decibel", "Frequency" e "kHz". Entrambe le stringhe sono in inglese e non sono mai localizzate. Il DMO può fornire le versioni localizzate tramite il metodo [**IMediaParamInfo:: GetParamText**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext) .

Le informazioni per ogni parametro rimangono fisse per tutto il ciclo di vita di DMO. Il client può quindi eseguire una query per ottenere queste informazioni una volta e quindi memorizzarle nella cache.

**Formati di ora**

Il client deve ora contrassegnare i dati di input, in modo che DMO possa calcolare i valori dei parametri corrispondenti. Per impostazione predefinita, i timestamp rappresentano unità di 100 nanosecondi, denominate anche *tempo di riferimento*. Questa unità di tempo non è tuttavia utile per ogni applicazione, pertanto un DMO ha un'opzione per supportare altri formati temporali. I formati di ora sono identificati dal GUID.



| **GUID**              | Descrizione                   |
|-----------------------|-------------------------------|
| \_riferimento ora \_ GUID | Ora riferimento                |
| \_tempo GUID \_ musica     | Note sulle parti per ogni trimestre (PPQN) |
| \_esempi di tempo GUID \_   | Campioni al secondo            |



 

Le terze parti sono incoraggiate a definire i propri formati di tempo in base alle esigenze. Tuttavia, tutti DMOs devono supportare l'ora di riferimento. Fornisce una baseline standard che tutti possono usare. Per determinare il numero di formati di ora supportati da DMO, chiamare il metodo [**IMediaParamInfo:: GetNumTimeFormats**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) . Per enumerare i formati supportati, chiamare il metodo [**IMediaParamInfo:: GetSupportedTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat) .

Per impostare il formato dell'ora, chiamare [**IMediaParams:: SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat). Questo metodo specifica il GUID del formato dell'ora e i *dati temporali*, ovvero il numero di unità per Tick del clock. Se, ad esempio, il formato dell'ora è Samples al secondo e i dati temporali sono 32, un valore di timestamp pari a 10 corrisponde a 320 campioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Parametri dei supporti](media-parameters.md)
</dt> </dl>

 

 



