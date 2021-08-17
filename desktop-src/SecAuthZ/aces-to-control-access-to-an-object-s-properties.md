---
description: ACE per controllare l'accesso alle proprietà di un oggetto
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACE per controllare l'accesso alle proprietà di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fddd5d78ff5b02bbbe4b9b7a7ce0b77d7be263f9fd3926f44411469af2bb3c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785253"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a>ACE per controllare l'accesso alle proprietà di un oggetto

[*L'elenco*](/windows/desktop/SecGloss/d-gly) di controllo di accesso discrezionale (DACL) di un oggetto del servizio directory può contenere una gerarchia di voci di controllo di accesso (ACE), come indicato di seguito: [](/windows/desktop/SecGloss/a-gly)

1.  ACE che proteggono l'oggetto stesso
2.  [ACE specifiche dell'oggetto](object-specific-aces.md) che proteggono un set di proprietà specificato nell'oggetto
3.  ACE specifiche dell'oggetto che proteggono una proprietà specificata nell'oggetto

All'interno di questa gerarchia, i diritti concessi o negati a un livello superiore si applicano anche ai livelli inferiori. Ad esempio, se una ACE specifica dell'oggetto in un set di proprietà consente a un trustee il diritto READ \_ \_ PROP DS ADS RIGHT, il \_ trustee ha accesso in lettura implicito a tutte le proprietà di tale \_ set di proprietà. Analogamente, una ACE sull'oggetto stesso che consente l'accesso ADS RIGHT DS READ PROP concede al \_ trustee l'accesso in lettura a tutte le \_ \_ proprietà \_ dell'oggetto.

La figura seguente mostra l'albero di un ipotetico oggetto DS e i relativi set di proprietà e proprietà.

![gerarchia di oggetti del servizio directory](images/accctrl2.png)

Si supponga di voler consentire l'accesso seguente alle proprietà di questo oggetto DS:

-   Consenti gruppo Autorizzazione di lettura/scrittura per tutte le proprietà dell'oggetto
-   Consentire a tutti gli altri utenti l'autorizzazione di lettura/scrittura per tutte le proprietà ad eccezione della proprietà D

A tale scopo, impostare le voci ACE nell'elenco DACL dell'oggetto, come illustrato nella tabella seguente.



| Fiduciario  | GUID oggetto    | Tipo ACE                  | Diritti di accesso                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| Gruppo A  | Nessuno           | ACE consentita per l'accesso        | ADS \_ RIGHT \_ DS \_ READ \_ PROP \| ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |
| Tutti | Set di proprietà 1 | Access-allowed object ACE | ADS \_ RIGHT \_ DS \_ READ \_ PROP \| ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |
| Tutti | Proprietà C     | Access-allowed object ACE | ADS \_ RIGHT \_ DS \_ READ \_ PROP \| ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |



 

La ACE per il gruppo A non dispone di un GUID di oggetto, ovvero consente l'accesso a tutte le proprietà dell'oggetto. L'ACE specifica dell'oggetto per il set di proprietà 1 consente a tutti gli utenti di accedere alle proprietà A e B. L'altra ACE specifica dell'oggetto consente a tutti gli utenti di accedere alla proprietà C. Si noti che, anche se questo elenco di controllo di accesso non dispone di ACE per accesso negato, nega implicitamente l'accesso alla proprietà D a tutti gli utenti ad eccezione del gruppo A.

Quando un utente tenta di accedere alla proprietà di un oggetto, il sistema controlla le ACE, in ordine, fino a quando l'accesso richiesto non viene concesso, negato o non sono presenti altre ACE. In questo caso, l'accesso viene negato in modo implicito.

Il sistema valuta:

-   Voci ACE che si applicano all'oggetto stesso
-   ACE specifiche dell'oggetto che si applicano al set di proprietà che contiene la proprietà a cui si accede
-   ACE specifiche dell'oggetto che si applicano alla proprietà a cui si accede

Il sistema ignora le voci ACE specifiche dell'oggetto che si applicano ad altri set di proprietà o proprietà.

 

 
