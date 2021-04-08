---
title: Mapping dell'interfaccia utente dell'oggetto gruppo
description: In questo argomento vengono descritte le finestre delle proprietà dell'oggetto gruppo nello snap-in utenti e computer di Active Directory. Proprietà generale SheetMember della proprietà SheetMembers della proprietà SheetManaged dalla finestra delle proprietà
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- Active Directory mapping dell'interfaccia utente oggetto
- Mapping dell'interfaccia utente, oggetto gruppo Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2277c24f621f8e32f46b9e9571d0d0d4de9cfc
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046505"
---
# <a name="group-object-user-interface-mapping"></a>Mapping dell'interfaccia utente dell'oggetto gruppo

In questo argomento vengono descritte le finestre delle proprietà dell'oggetto gruppo nello snap-in utenti e computer di Active Directory.

-   [Finestra delle proprietà generale](#general-property-sheet)
-   [Membro della finestra delle proprietà](#member-of-property-sheet)
-   [Finestra delle proprietà dei membri](#members-property-sheet)
-   [Gestito da finestra delle proprietà](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>Finestra delle proprietà generale

Nella tabella seguente vengono illustrate le etichette dell'interfaccia utente della finestra delle proprietà **generale** .



| Etichetta interfaccia utente                      | Attributo in Active Directory Domain Services     |
|-------------------------------|---------------------------------------------------|
| Nome gruppo (precedente a Windows 2000) | [**Nome account SAM**](/windows/desktop/ADSchema/a-samaccountname) |
| Descrizione                   | [**Descrizione**](/windows/desktop/ADSchema/a-description)         |
| Posta elettronica                        | [**Indirizzi di posta elettronica**](/windows/desktop/ADSchema/a-mail)           |
| Ambito gruppo                   | [**Tipo di gruppo**](/windows/desktop/ADSchema/a-grouptype)            |
| Tipo di gruppo                    | [**Tipo di gruppo**](/windows/desktop/ADSchema/a-grouptype)            |
| Note                         | [**Commento**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>Membro della finestra delle proprietà

Nella tabella seguente vengono illustrate le etichette dell'interfaccia utente del **membro della finestra delle** proprietà.



| Etichetta interfaccia utente  | Attributo in Active Directory Domain Services | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro di | [**Is-member-of-DL**](/windows/desktop/ADSchema/a-memberof)    | Contiene i nomi distinti dei gruppi a cui appartiene il gruppo. L'attributo member di ogni gruppo in questo elenco contiene il nome distinto di questo oggetto gruppo. L'interfaccia utente non modifica direttamente l'attributo [**is-member-of-DL**](/windows/desktop/ADSchema/a-memberof) . Modifica l'attributo [**member**](/windows/desktop/ADSchema/a-member) nell'oggetto Group di cui è membro l'oggetto. Il server di Active Directory gestisce l'attributo **is-member-of-DL** .<br/> |



 

## <a name="members-property-sheet"></a>Finestra delle proprietà dei membri

Nella tabella seguente vengono illustrate le etichette dell'interfaccia utente della finestra delle proprietà dei **membri** .



| Etichetta interfaccia utente | Attributo in Active Directory Domain Services | Descrizione                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| Membri  | [**Membro**](/windows/desktop/ADSchema/a-member)               | Contiene i nomi distinti dei membri di questo oggetto gruppo. |



 

## <a name="managed-by-property-sheet"></a>Gestito da finestra delle proprietà

Nella tabella seguente vengono illustrate le etichette dell'interfaccia utente della finestra delle proprietà **gestite da** .



| Etichetta interfaccia utente                           | Attributo in Active Directory Domain Services                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nome                               | [**Gestito da**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Il responsabile può aggiornare l'elenco di appartenenze | Nessuna. Viene aggiunta una voce ACE con l'autorizzazione "Consenti-scrittura membri" all'account identificato in base al **nome**.                        |
| Office                             | L'attributo [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) dell'account identificato in base al **nome**. |
| Indirizzo                             | Attributo [**via-indirizzo**](/windows/desktop/ADSchema/a-street) dell'account identificato in base al **nome**.                                    |
| City                               | Attributo [**Locality-Name**](/windows/desktop/ADSchema/a-l) dell'account identificato in base al **nome**.                                          |
| Provincia                     | Attributo [**state-o-Province-Name**](/windows/desktop/ADSchema/a-st) dell'account identificato in base al **nome**.                                |
| Paese/Area geografica                     | Attributo [**Country-Name**](/windows/desktop/ADSchema/a-c) dell'account identificato in base al **nome**.                                           |
| Numero di telefono                   | Attributo del [**numero telefonico**](/windows/desktop/ADSchema/a-telephonenumber) dell'account identificato in base al **nome**.                         |
| Numero fax                         | L'attributo [**Fax-Phone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) dell'account identificato in base al **nome**.      |



 

 

