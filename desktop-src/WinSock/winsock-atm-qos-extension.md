---
description: In questa sezione viene descritta la struttura di qualità del servizio (QOS) specifica del protocollo per ATM, che è contenuto nel campo ProviderSpecific della struttura QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Estensione QoS ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129106"
---
# <a name="winsock-atm-qos-extension"></a>Estensione QoS ATM Winsock

In questa sezione viene descritta la struttura di qualità del servizio ([**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)) specifica del protocollo per ATM, che è contenuto nel campo [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) della struttura **QoS** . Si noti che l'utilizzo di questa struttura **QoS** specifica di ATM è facoltativo per i client Windows Sockets 2 e che il provider di servizi ATM è necessario per eseguire il mapping della struttura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) generica agli elementi di informazioni Q. 2931 appropriati. Tuttavia, se vengono specificate sia la struttura **FLOWSPEC** generica che la struttura **QoS** specifica di ATM, il valore specificato nella struttura **QoS** specifica di ATM avrà la precedenza in caso di conflitti. Vedere la sezione 2,7 della specifica dell'API di Windows Sockets 2 per altre informazioni sulle disposizioni QoS e sulla struttura **FLOWSPEC** .

La struttura [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) specifica del protocollo per ATM è una concatenazione di strutture dell'elemento informazioni Q. 2931, definite nel testo seguente. Se un'applicazione omette un IE che UNI 3. x impone, il provider di servizi deve inserire un valore predefinito ragionevole, prendendo in considerazione le informazioni contenute nella struttura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) , se applicabile.

La gestione di IEs ripetute dipende dallo stesso IE. Se un IE viene ripetuto ed è uno che può essere ripetuto in base alla specifica UNI del forum ATM, il provider deve gestirlo correttamente. In questo caso, l'ordine nell'elenco determina l'ordine delle preferenze, con la preferenza per gli elementi visualizzati in precedenza nell'elenco. Se un IE viene ripetuto e questa operazione non è consentita per la specifica UNI del forum ATM, il provider potrebbe non riuscire a eseguire la richiesta dal client (opzione preferita) o usare l'ultimo IE di quel tipo trovato.

Ogni singola struttura di IE viene formattata nel modo seguente e identificata dal campo **IEType** :

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

I valori validi per il campo **IEType** sono definiti come segue:

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

Il campo **IE** viene sovrapposto a una struttura di IE specifica e il campo **IELength** è la lunghezza totale, in byte, della struttura di IE, inclusi i campi **IEType** e **IELength** . La semantica e i valori validi per ogni elemento di queste strutture IE sono per ogni specifica ATM UNI 3. x. È \_ \_ possibile usare il campo SAP assente per gli elementi facoltativi per una determinata struttura di IE, per ogni specifica ATM UNI 3. x.

 

 
