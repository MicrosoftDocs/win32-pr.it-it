---
description: Registrazione e annullamento della registrazione delle chiavi
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrazione e annullamento della registrazione delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315443"
---
# <a name="registering-and-deregistering-keys"></a>Registrazione e annullamento della registrazione delle chiavi

## <a name="registering-keys"></a>Registrazione di chiavi

Un nodo può registrare le chiavi con [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) in qualsiasi momento mentre si trovino in **DRT \_ Active**, **DRT \_ alone** e **DRT senza stati di \_ \_ rete** . Le chiavi registrate **solo \_ in DRT** e **DRT nessun stato di \_ \_ rete** possono essere riconosciute solo da altri DRTS dopo che il nodo locale è passato a **DRT \_ attivo**.

Non è possibile registrare chiavi identiche all'interno della stessa istanza di DRT quando si usa [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider). Se viene tentata la registrazione di chiavi identiche, la registrazione della seconda chiave avrà esito negativo. Anche l'uso di chiavi identiche deve essere evitato tra istanze DRT diverse. Esegue una ricerca in base alla designazione di chiave univoca. questa condivisione di chiavi identica può restituire una qualsiasi delle chiavi, indipendentemente dai dati associati alla chiave.

> [!Note]  
> Se è necessario un comportamento diverso per l'implementazione, è possibile creare un provider di sicurezza al posto di [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) .

 

## <a name="deregistering-keys"></a>Annullamento della registrazione delle chiavi

Un nodo può annullare la registrazione di una chiave in qualsiasi momento dopo che è stata registrata. Tuttavia, solo l'applicazione che ha registrato la chiave può annullarne la registrazione. Un'applicazione può annullare la registrazione di una chiave dal nodo locale usando la funzione [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) . Al termine, la funzione attiva un evento di **\_ \_ \_ \_ modifica della chiave LEAFSET di un evento DRT** ; informa l'applicazione e gli altri nodi che partecipano alla rete DRT.

Durante lo stato **di \_ errore DRT** , la chiamata obbligatoria di [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) comporterà l'annullamento della registrazione di tutte le chiavi da parte dell'infrastruttura DRT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca in una tabella di routing distribuita](searching-a-distributed-routing-table.md)
</dt> <dt>

[Informazioni sulle tabelle di routing distribuite](about-distributed-routing-tables.md)
</dt> <dt>

[Riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



