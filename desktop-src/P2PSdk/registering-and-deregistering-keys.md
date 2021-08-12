---
description: Registrazione e annullamento della registrazione delle chiavi
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrazione e annullamento della registrazione delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d586fc2bf399a30b8a962611a21a4e0994d88f4513453c071b110de1d4142b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612164"
---
# <a name="registering-and-deregistering-keys"></a>Registrazione e annullamento della registrazione delle chiavi

## <a name="registering-keys"></a>Registrazione delle chiavi

Un nodo può registrare le chiavi con [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) in qualsiasi momento negli stati **DRT \_ ACTIVE**, **DRT \_ ALONE** e **DRT \_ NO \_ NETWORK.** Le chiavi registrate negli **stati DRT \_ ALONE** e **DRT \_ NO \_ NETWORK** possono essere riconosciute da altri DRT solo dopo la transizione del nodo locale a **DRT \_ ACTIVE**.

Non è possibile registrare chiavi identiche nella stessa istanza DRT quando si [**usa DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider). Se viene tentata la registrazione di chiavi identiche, la registrazione della seconda chiave avrà esito negativo. È anche consigliabile evitare l'uso di chiavi identiche tra istanze DRT diverse. Le ricerche nella designazione di chiave univoca di queste condivisioni di chiavi identiche possono restituire una qualsiasi delle chiavi, indipendentemente dai dati associati alla chiave.

> [!Note]  
> Se è necessario un comportamento diverso per l'implementazione, è possibile creare un provider di sicurezza al posto di [**DrtCreateDerivedKeySecurityProvider.**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider)

 

## <a name="deregistering-keys"></a>Annullamento della registrazione delle chiavi

Un nodo può annullare la registrazione di una chiave in qualsiasi momento dopo la registrazione. Tuttavia, solo l'applicazione che ha registrato la chiave può annullarla. Un'applicazione può annullare la registrazione di una chiave dal nodo locale usando la [**funzione DrtUnregisterKey.**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) Al termine, la funzione attiva un evento **DRT \_ EVENT \_ LEAFSET \_ KEY \_ CHANGE,** informando l'applicazione e altri nodi che partecipano alla mesh DRT.

Nello stato **DRT \_ FAULTED,** la chiamata richiesta di [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) comporterà l'annullamento della registrazione di tutte le chiavi da parte dell'infrastruttura DRT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca di una tabella di routing distribuito](searching-a-distributed-routing-table.md)
</dt> <dt>

[Informazioni sulle tabelle di routing distribuito](about-distributed-routing-tables.md)
</dt> <dt>

[Informazioni di riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



