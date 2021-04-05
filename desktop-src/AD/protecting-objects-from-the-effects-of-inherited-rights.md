---
title: Protezione di oggetti dagli effetti dei diritti ereditati
description: Come illustrato nell'argomento ereditarietà e delega dell'amministrazione, le voci ACE possono essere impostate su un oggetto contenitore, ad esempio organizationalUnit, domainDNS, container e così via, e propagate agli oggetti figlio in base ai flag ACE impostati su tali ACE.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protezione di oggetti dagli effetti di Active Directory con diritti ereditati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046497"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>Protezione di oggetti dagli effetti dei diritti ereditati

Come illustrato nell'argomento [ereditarietà e delega dell'amministrazione](inheritance-and-delegation-of-administration.md), le voci ACE possono essere impostate su un oggetto contenitore, ad esempio **OrganizationalUnit**, **domainDNS**, **container** e così via, e propagate agli oggetti figlio in base ai flag ACE impostati su tali ACE.

Se si dispone di un oggetto protetto o di un oggetto le cui voci ACE si desidera controllare in modo esplicito, ad esempio un'unità organizzativa privata o un utente speciale, è possibile impedire la propagazione delle voci ACE all'oggetto tramite il contenitore padre o i predecessori del contenitore padre.

Utilizzare la proprietà [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per controllare se i DACL e i SACL vengono ereditati dall'oggetto dal relativo contenitore padre.

È possibile usare la proprietà [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per proteggere un oggetto dagli effetti delle voci ACE ereditate. I flag seguenti consentono di impostare in modo esplicito il controllo di accesso sull'oggetto e impedire a un utente di modificare il controllo di accesso all'oggetto impostando le voci ACE ereditabili sul contenitore padre dell'oggetto o i predecessori del relativo contenitore padre.



| Flag                               | Descrizione                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_elenco DACL se \_ protetto**<br/> | Impedisce l'applicazione degli ACE impostati sull'elenco DACL del contenitore padre e di tutti gli oggetti sopra il contenitore padre nella gerarchia di directory, dall'applicazione all'oggetto DACL.<br/> |
| **SE \_ SACL è \_ protetto**<br/> | Impedisce l'applicazione di Ace impostati sull'elenco SACL del contenitore padre e di tutti gli oggetti sopra il contenitore padre nella gerarchia di directory, dall'applicazione al SACL dell'oggetto.<br/> |



 

Tenere presente che il flag di **\_ \_ presenza DACL se** deve essere presente per impostare **se \_ DACL \_ protected** e **se SACL è \_ \_ presente** devono essere presenti per impostare **se \_ SACL \_ protected**.

 

