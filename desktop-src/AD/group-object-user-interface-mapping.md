---
title: Mapping dell'Interfaccia utente gruppo
description: In questo argomento vengono descritte le finestre delle proprietà dell'oggetto Group Utenti e computer di Active Directory snap-in. Finestra delle proprietà GeneraleMembro della finestra delle proprietà Foglio delle proprietà MembriManaged by Property Sheet
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- Mapping di Active Directory Interfaccia utente oggetti gruppo
- Interfaccia utente Mapping, Group Object AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308b3bafc24f8b8419b23c351d981f4f01961885cd535ac2d24b96cd62e17633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188965"
---
# <a name="group-object-user-interface-mapping"></a>Mapping dell'Interfaccia utente gruppo

In questo argomento vengono descritte le finestre delle proprietà dell'oggetto Group Utenti e computer di Active Directory snap-in.

-   [Finestra delle proprietà Generale](#general-property-sheet)
-   [Membro della finestra delle proprietà](#member-of-property-sheet)
-   [Finestra delle proprietà Membri](#members-property-sheet)
-   [Finestra delle proprietà Gestita da](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>Finestra delle proprietà Generale

La tabella seguente mostra le etichette dell'interfaccia utente della **finestra delle proprietà** Generale.



| Etichetta dell'interfaccia utente                      | Attributo in Active Directory Domain Services     |
|-------------------------------|---------------------------------------------------|
| Nome gruppo (versione Windows 2000) | [**SAM-Account-Name**](/windows/desktop/ADSchema/a-samaccountname) |
| Descrizione                   | [**Descrizione**](/windows/desktop/ADSchema/a-description)         |
| Posta elettronica                        | [**Indirizzi di posta elettronica**](/windows/desktop/ADSchema/a-mail)           |
| Ambito gruppo                   | [**Tipo di gruppo**](/windows/desktop/ADSchema/a-grouptype)            |
| Tipo di gruppo                    | [**Tipo di gruppo**](/windows/desktop/ADSchema/a-grouptype)            |
| Note                         | [**Commento**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>Membro della finestra delle proprietà

La tabella seguente mostra le etichette dell'interfaccia utente della **finestra delle proprietà Membro** di.



| Etichetta dell'interfaccia utente  | Attributo in Active Directory Domain Services | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro di | [**Is-Member-Of-DL**](/windows/desktop/ADSchema/a-memberof)    | Contiene i nomi distinti dei gruppi a cui appartiene questo gruppo. L'attributo member di ogni gruppo in questo elenco contiene il nome distinto di questo oggetto gruppo. L'interfaccia utente non modifica direttamente [**l'attributo Is-Member-Of-DL.**](/windows/desktop/ADSchema/a-memberof) Modifica [**l'attributo Member**](/windows/desktop/ADSchema/a-member) nell'oggetto gruppo di cui l'oggetto è membro. Il server Active Directory gestisce **l'attributo Is-Member-Of-DL.**<br/> |



 

## <a name="members-property-sheet"></a>Finestra delle proprietà Membri

La tabella seguente mostra le etichette dell'interfaccia utente della **finestra delle proprietà** Membri.



| Etichetta dell'interfaccia utente | Attributo in Active Directory Domain Services | Descrizione                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| Membri  | [**Membro**](/windows/desktop/ADSchema/a-member)               | Contiene i nomi distinti dei membri di questo oggetto gruppo. |



 

## <a name="managed-by-property-sheet"></a>Finestra delle proprietà Gestita da

La tabella seguente mostra le etichette dell'interfaccia utente della **finestra delle proprietà Managed By.**



| Etichetta dell'interfaccia utente                           | Attributo in Active Directory Domain Services                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nome                               | [**Gestito da**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Manager può aggiornare l'elenco di appartenenze | Nessuno. Viene aggiunta una ACE con l'autorizzazione "Consenti - Scrittura membri" all'account identificato da **Nome**.                        |
| Office                             | Attributo [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) dell'account identificato da **Name**. |
| Indirizzo                             | Attributo [**Street-Address**](/windows/desktop/ADSchema/a-street) dell'account identificato da **Name**.                                    |
| City                               | Attributo [**Locality-Name dell'account**](/windows/desktop/ADSchema/a-l) identificato da **Name**.                                          |
| Provincia                     | Attributo [**State-Or-Province-Name**](/windows/desktop/ADSchema/a-st) dell'account identificato da **Name**.                                |
| Paese/Area geografica                     | Attributo [**Country-Name**](/windows/desktop/ADSchema/a-c) dell'account identificato da **Name**.                                           |
| Numero di telefono                   | Attributo [**Telephone-Number**](/windows/desktop/ADSchema/a-telephonenumber) dell'account identificato da **Name**.                         |
| Numero fax                         | Attributo [**Facsimile-Telephone-Number dell'account**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) identificato da **Name**.      |



 

 

