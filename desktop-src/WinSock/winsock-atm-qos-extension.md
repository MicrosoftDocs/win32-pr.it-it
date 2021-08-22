---
description: Questa sezione descrive la struttura QOS (Quality of Service) specifica del protocollo per ATM, contenuta nel campo ProviderSpecific della struttura QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Estensione QoS di Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422db2df8e4f845086120814f6cf4e6288dcc00c42693eac8da21c466448aaa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612821"
---
# <a name="winsock-atm-qos-extension"></a>Estensione QoS di Winsock ATM

Questa sezione descrive la struttura [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)(Quality of Service) specifica del protocollo per ATM, contenuta nel campo [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) della **struttura QOS.** Si noti che l'uso di questa struttura **QOS** specifica di ATM è facoltativo dai client Windows Sockets 2 e che il provider di servizi ATM è necessario per eseguire il mapping della struttura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) generica agli elementi di informazioni Q.2931 appropriati. Tuttavia, se vengono specificate sia la struttura **GENERICA FLOWSPEC** che la struttura **QOS** specifica di ATM, il valore specificato nella struttura **QOS** specifica di ATM deve avere la precedenza in caso di conflitti. Per Windows provisioning QoS e la struttura **FLOWSPEC,** vedere la sezione 2.7 della specifica api di Windows Sockets 2.

La struttura [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) specifica del protocollo per ATM è una concatenazione delle strutture degli elementi di informazioni Q.2931, definite nel testo seguente. Se un'applicazione omette un IE che UNI 3.x impone, il provider di servizi deve inserire un valore predefinito ragionevole, tenendo conto delle informazioni nella struttura [**FLOWSPEC,**](/windows/win32/api/qos/ns-qos-flowspec) se applicabile.

La gestione di IE ripetuti dipende dall'IE stesso. Se un'istanza di IE viene ripetuta e può essere ripetuta in base alla specifica UNI del forum ATM, il provider deve gestirlo correttamente. In questo caso, l'ordine nell'elenco determina l'ordine delle preferenze, con gli elementi visualizzati in precedenza nell'elenco come preferiti. Se viene ripetuto UnE e questa operazione non è consentita in base alla specifica UNI del forum ATM, il provider potrebbe non riuscire la richiesta dal client (opzione preferita) o usare l'ultimo IE di quel tipo trovato.

Ogni singola struttura di IE viene formattata nel modo seguente e identificata dal **campo IEType:**

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

I valori validi per **il campo IEType** sono definiti come:

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

Il **campo IE** è sovrapposto da una struttura di IE specifica e il campo **IELength** è la lunghezza totale in byte della struttura di IE, inclusi i campi **IEType** e **IELength.** La semantica e i valori validi per ogni elemento di queste strutture di IE sono in base alla specifica ATM UNI 3.x. SAP FIELD ABSENT può essere usato per gli elementi facoltativi per una determinata struttura \_ \_ di IE, in base alla specifica UNI 3.x di ATM.

 

 
