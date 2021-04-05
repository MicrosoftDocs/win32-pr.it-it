---
title: Specifica dell'ambito di ricerca
description: È possibile specificare l'ambito di una ricerca come una ricerca di base, di un livello o di un sottoalbero.
ms.assetid: b02354c2-7b95-4911-8ae3-4a261d3ca2d3
ms.tgt_platform: multiple
keywords:
- Specifica dell'ambito di ricerca Active Directory
- Active Directory, ricerca, specifica dell'ambito di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ff076e0410088c69eace25f204241c1c51c6fb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724434"
---
# <a name="specifying-the-search-scope"></a>Specifica dell'ambito di ricerca

È possibile specificare l'ambito di una ricerca come una ricerca di base, di un livello o di un sottoalbero. Usare il flag dell' **\_ ambito di \_ ricerca \_ ADS SEARCHPREF** con i valori dell'enumerazione [**\_ SCOPEENUM ADS**](/windows/win32/api/iads/ne-iads-ads_scopeenum) per specificare l'ambito di ricerca. Nell'elenco seguente sono incluse le descrizioni dei tipi di ricerca:

-   Di **base**. Una ricerca di base limita la ricerca all'oggetto di base. Il numero massimo di oggetti restituiti è sempre uno. Questa ricerca è utile per verificare l'esistenza di un oggetto per il recupero dell'appartenenza al gruppo. Se, ad esempio, si dispone di un nome distinto dell'oggetto ed è necessario verificare l'esistenza dell'oggetto in base al percorso, è possibile utilizzare una ricerca a un solo livello. Se la ricerca ha esito negativo, è possibile presupporre che l'oggetto sia stato rinominato o spostato in un percorso diverso oppure che siano state fornite informazioni errate sull'oggetto. Tenere presente che è necessario archiviare l'identificatore univoco globale (GUID) dell'oggetto anziché il nome distinto, se si vuole rivedere un oggetto. Il GUID fa sempre riferimento allo stesso oggetto, indipendentemente dalla posizione in cui si trova l'oggetto all'interno della gerarchia di directory.
-   **Un livello**. Una ricerca a un solo livello è limitata agli elementi figlio immediati di un oggetto di base, ma esclude l'oggetto di base stesso. Questa impostazione può eseguire una ricerca di destinazione per gli oggetti figlio immediati di un oggetto padre. Si consideri, ad esempio, un oggetto padre P1 e i relativi elementi figlio immediati: C1, C2 e C3. Una ricerca a un solo livello valuta C1, C2 e C3 rispetto ai criteri di ricerca, ma non valuta P1. Utilizzare una ricerca a un livello per enumerare tutti gli elementi figlio di un oggetto. Un'enumerazione [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) viene convertita in una ricerca a un solo livello.
-   **Sottoalbero**. Una ricerca di sottoalbero (o una ricerca completa) include tutti gli oggetti figlio e l'oggetto di base. È possibile richiedere al provider LDAP di inseguire i riferimenti ad altri servizi directory LDAP, inclusi altri domini o foreste di directory.

 

 