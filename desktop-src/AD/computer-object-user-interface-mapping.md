---
title: Mapping dell'interfaccia utente dell'oggetto computer
description: Nelle tabelle seguenti sono elencati gli elementi delle finestre delle proprietà dell'oggetto computer nello snap-in Active Directory utenti e computer.
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724615"
---
# <a name="computer-object-user-interface-mapping"></a>Mapping dell'interfaccia utente dell'oggetto computer

Nelle tabelle seguenti sono elencati gli elementi delle finestre delle proprietà dell'oggetto computer nello snap-in Active Directory utenti e computer.

## <a name="general-property-sheet"></a>Finestra delle proprietà generale

Nella tabella seguente sono elencate le etichette dell'interfaccia utente della finestra delle proprietà **generale** .



| Etichetta interfaccia utente                         | Attributo Active Directory Domain Services | Commenti                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| Nome computer (precedente a Windows 2000) | sAMAccountName                             |                                                  |
| Nome DNS                         | dNSHostName                                |                                                  |
| Ruolo                             | userAccountControl                         | Imposta un bit nella maschera di bit userAccountControl. |
| Descrizione                      | description                                |                                                  |
| Computer attendibile per la delega    | userAccountControl                         | Imposta un bit nella maschera di bit userAccountControl. |



 

## <a name="location-property-sheet"></a>Finestra delle proprietà Location

La tabella seguente elenca le etichette dell'interfaccia utente della finestra delle proprietà **location** .



| Etichetta interfaccia utente | Attributo Active Directory Domain Services |
|----------|--------------------------------------------|
| Location | posizione                                   |



 

## <a name="member-of-property-sheet"></a>Membro della finestra delle proprietà

Nella tabella seguente sono elencate le etichette dell'interfaccia utente del **membro della finestra delle** proprietà.



| Etichetta interfaccia utente          | Attributo Active Directory Domain Services | Commenti                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro di         | memberOf                                   | Include tutti i gruppi nell'elenco dell'interfaccia utente, ad eccezione del gruppo primario, rappresentato nell'annuncio tramite l'attributo [**primaryGroupID**](/windows/desktop/ADSchema/a-primarygroupid) . |
| Imposta gruppo primario | primaryGroupID                             | LDAP: associato a [**PrimaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del gruppo primario.                                                                                  |



 

## <a name="operating-system-property-sheet"></a>Finestra delle proprietà del sistema operativo

Nella tabella seguente sono elencate le etichette dell'interfaccia utente della finestra delle proprietà del **sistema operativo** .



| Etichetta interfaccia utente     | Attributo Active Directory Domain Services |
|--------------|--------------------------------------------|
| Nome         | operatingSystem                            |
| Versione      | operatingSystemVersion                     |
| Service Pack | operatingSystemServicePack                 |



 

 

 