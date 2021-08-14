---
title: Protezione degli oggetti dagli effetti dei diritti ereditati
description: Come illustrato nell'argomento Ereditarietà e delega dell'amministrazione, le voci ACE possono essere impostate su un oggetto contenitore, ad esempio organizationalUnit, domainDNS, contenitore e così via, e propagate agli oggetti figlio in base ai flag ACE impostati su tali ACE.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protezione degli oggetti dagli effetti dei diritti ereditati di ACTIVE Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcc1067fcfe0d57e2e7aca837b97d73f18b55a41a4f1347ac36224b987918aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185016"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>Protezione degli oggetti dagli effetti dei diritti ereditati

Come illustrato nell'argomento Ereditarietà e delega dell'amministrazione, [](inheritance-and-delegation-of-administration.md)le voci ACE possono essere impostate su un oggetto contenitore, ad esempio **organizationalUnit,** **domainDNS,** **container** e così via, e propagate agli oggetti figlio in base ai flag ACE impostati su tali ACE.

Se si dispone di un oggetto protetto o di un oggetto di cui si desidera controllare in modo esplicito le voci ACE, ad esempio un'unità organizzativa privata o un utente speciale, è possibile impedire la propagazione delle voci ACE all'oggetto dal contenitore padre o dai predecessori del contenitore padre.

Usare la [**proprietà IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per controllare se i DACL e i SACL vengono ereditati dall'oggetto dal contenitore padre.

La [**proprietà IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) può essere usata per proteggere un oggetto dagli effetti delle ACE ereditate. I flag seguenti forzano l'impostazione esplicita del controllo di accesso sull'oggetto e impediscono a un utente di modificare il controllo di accesso per l'oggetto impostando le voci ACE ereditabili nel contenitore padre dell'oggetto o nei predecessori del contenitore padre.



| Flag                               | Descrizione                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_edizione Standard DACL \_ PROTETTO**<br/> | Impedisce che le voci ACE impostate nell'elenco DACL del contenitore padre e tutti gli oggetti al di sopra del contenitore padre nella gerarchia di directory vengano applicati all'elenco DACL dell'oggetto.<br/> |
| **\_edizione Standard SACL \_ PROTETTO**<br/> | Impedisce l'applicazione di voci ACE impostate nel SACL del contenitore padre e di tutti gli oggetti al di sopra del contenitore padre nella gerarchia di directory all'oggetto SACL.<br/> |



 

Tenere presente il flag **\_ EDIZIONE STANDARD DACL \_ PRESENT** per impostare **edizione Standard \_ DACL \_ PROTECTED** e **edizione Standard \_ SACL \_ PRESENT** per impostare edizione Standard **\_ SACL \_ PROTECTED**.

 

