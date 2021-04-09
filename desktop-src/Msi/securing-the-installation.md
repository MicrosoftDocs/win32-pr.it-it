---
description: Aggiungere tutte le proprietà della password dalla tabella CustomUserAccounts alla proprietà MsiHiddenProperties nella tabella delle proprietà.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Sicurezza dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968672"
---
# <a name="securing-the-installation"></a>Sicurezza dell'installazione

Aggiungere tutte le proprietà della password dalla tabella CustomUserAccounts alla proprietà [**MsiHiddenProperties**](msihiddenproperties.md) nella [tabella delle proprietà](property-table.md). Aggiungere anche i nomi delle azioni personalizzate posticipate alla proprietà **MsiHiddenProperties** . Ciò impedirà al programma di installazione di scrivere i valori delle proprietà sensibili (le password) nel log e garantirà che questi valori non vengano registrati quando le azioni personalizzate posticipate utilizzano i valori come proprietà CustomActionData.

Affinché la password dell'utente sia disponibile nel servizio Windows Installer, è necessario aggiungere la proprietà password alla proprietà [**SecureCustomProperties**](securecustomproperties.md) .

[Tabella delle proprietà](property-table.md)



| Proprietà                                                 | Valore                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**MsiHiddenProperties**](msihiddenproperties.md)       | TESTUSERPASSWORD; CreateAccount RemoveAccount RollbackAccount |
| [**SecureCustomProperties**](securecustomproperties.md) | TESTUSERPASSWORD                                             |



 

Si conclude l'esempio.

 

 



