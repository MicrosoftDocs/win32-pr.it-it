---
title: Mapping Interfaccia utente unità organizzative
description: In questo argomento vengono descritte le finestre delle proprietà dell'oggetto unità organizzativa nello snap-in Utenti e computer di Active Directory di lavoro.
ms.assetid: 105c0f01-55d5-4dc2-887e-5e204ba82c4c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34d4f3e268e9448e9b835a4716cfa3f379ffb3cac93c2720e3f455a66384ed32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025519"
---
# <a name="organizational-unit-user-interface-mapping"></a>Mapping Interfaccia utente unità organizzative

In questo argomento vengono descritte le finestre delle proprietà dell'oggetto unità organizzativa nello snap-in Utenti e computer di Active Directory di lavoro.

## <a name="general-property-sheet"></a>Finestra delle proprietà Generale

La tabella seguente mostra le etichette dell'interfaccia utente della **finestra delle proprietà** Generale.



| Etichetta dell'interfaccia utente        | Attributo in Active Directory Domain Services |
|-----------------|-----------------------------------------------|
| Descrizione     | [**Descrizione**](/windows/desktop/ADSchema/a-description)     |
| Indirizzo          | [**Via**](/windows/desktop/ADSchema/a-street)       |
| City            | [**Locality-Name**](/windows/desktop/ADSchema/a-l)             |
| Provincia  | [**State-Or-Province-Name**](/windows/desktop/ADSchema/a-st)   |
| CAP | [**Codice postale**](/windows/desktop/ADSchema/a-postalcode)      |
| Paese/Area geografica  | [**Nome paese**](/windows/desktop/ADSchema/a-c)              |



 

## <a name="managed-by-property-sheet"></a>Finestra delle proprietà Gestita da

La tabella seguente mostra le etichette dell'interfaccia utente della **finestra delle proprietà Managed By.**



| Etichetta dell'interfaccia utente         | Attributo in Active Directory Domain Services                                                                                   |
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nome             | [**Gestito da**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Office           | Attributo [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) dell'account identificato da **Name**. |
| Indirizzo           | Attributo [**Street-Address**](/windows/desktop/ADSchema/a-street) dell'account identificato da **Name**.                                    |
| City             | Attributo [**Locality-Name dell'account**](/windows/desktop/ADSchema/a-l) identificato da **Name**.                                          |
| Provincia   | Attributo [**State-Or-Province-Name**](/windows/desktop/ADSchema/a-st) dell'account identificato da **Name**.                                |
| Paese/Area geografica   | Attributo [**Country-Name**](/windows/desktop/ADSchema/a-c) dell'account identificato da **Name**.                                           |
| Numero di telefono | Attributo [**Telephone-Number**](/windows/desktop/ADSchema/a-telephonenumber) dell'account identificato da **Name**.                         |
| Numero fax       | Attributo [**Facsimile-Telephone-Number dell'account**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) identificato da **Name**.      |



 

 

 