---
description: Aggiungere tutte le proprietà Password della tabella CustomUserAccounts alla proprietà MsiHiddenProperties nella tabella Property.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Protezione dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642170cc2ac4e84bebe5235e84328abe5039ede1bdb8fc2760bbd249ff5268de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040731"
---
# <a name="securing-the-installation"></a>Protezione dell'installazione

Aggiungere tutte le proprietà Password dalla tabella CustomUserAccounts alla [**proprietà MsiHiddenProperties**](msihiddenproperties.md) nella [tabella Property](property-table.md). Aggiungere i nomi delle azioni personalizzate posticipate anche **alla proprietà MsiHiddenProperties.** Ciò impedirà al programma di installazione di scrivere i valori delle proprietà sensibili (password) nel log e garantirà che questi valori non vengono registrati quando le azioni personalizzate posticipate usano i valori come proprietà CustomActionData.

Perché la password dell'utente sia disponibile nel servizio Windows Installer, è necessario aggiungere la proprietà password [**alla proprietà SecureCustomProperties.**](securecustomproperties.md)

[Tabella delle proprietà](property-table.md)



| Proprietà                                                 | Valore                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**MsiHiddenProperties**](msihiddenproperties.md)       | TESTUSERPASSWORD; CreateAccount; RemoveAccount; RollbackAccount |
| [**SecureCustomProperties**](securecustomproperties.md) | TESTUSERPASSWORD                                             |



 

Questo conclude l'esempio.

 

 



