---
description: ACE per controllare l'accesso alle proprietà di un oggetto
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACE per controllare l'accesso alle proprietà di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227186"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a>ACE per controllare l'accesso alle proprietà di un oggetto

L' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) di un oggetto servizio directory (DS) può contenere una gerarchia di [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE), come indicato di seguito:

1.  ACE che proteggono l'oggetto stesso
2.  [Voci ACE specifiche dell'oggetto](object-specific-aces.md) che proteggono una proprietà specificata impostata nell'oggetto
3.  Voci ACE specifiche dell'oggetto che proteggono una proprietà specificata nell'oggetto

All'interno di questa gerarchia, i diritti concessi o negati a un livello superiore sono validi anche per i livelli inferiori. Se, ad esempio, una voce ACE specifica dell'oggetto in un set di proprietà consente a un trustee il diritto di \_ \_ lettura di un dominio ADS \_ \_ , il trustee ha accesso in lettura implicito a tutte le proprietà di tale set di proprietà. Analogamente, una voce ACE nell'oggetto stesso che consente ADS \_ Rights \_ DS \_ Read \_ prop Access fornisce al trustee l'accesso in lettura a tutte le proprietà dell'oggetto.

Nella figura seguente viene illustrata la struttura ad albero di un oggetto DS ipotetico e dei relativi set di proprietà e proprietà.

![gerarchia di oggetti del servizio directory](images/accctrl2.png)

Si supponga di voler consentire il seguente accesso alle proprietà di questo oggetto DS:

-   Consenti al gruppo un'autorizzazione di lettura/scrittura per tutte le proprietà dell'oggetto
-   Consenti a tutti gli utenti l'autorizzazione di lettura/scrittura per tutte le proprietà ad eccezione della proprietà D

A tale scopo, impostare le voci ACE nel DACL dell'oggetto, come illustrato nella tabella seguente.



| Fiduciario  | GUID oggetto    | Tipo ACE                  | Diritti di accesso                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| Gruppo A  | nessuno           | ACE consentito per l'accesso        | ADS \_ Rights \_ DS \_ Read \_ prop \| Ads \_ right \_ DS \_ scrivere \_ prop |
| Tutti | Set di proprietà 1 | ACE oggetto consentito Access | ADS \_ Rights \_ DS \_ Read \_ prop \| Ads \_ right \_ DS \_ scrivere \_ prop |
| Tutti | Proprietà C     | ACE oggetto consentito Access | ADS \_ Rights \_ DS \_ Read \_ prop \| Ads \_ right \_ DS \_ scrivere \_ prop |



 

La voce ACE per il gruppo A non ha un GUID oggetto, il che significa che consente l'accesso a tutte le proprietà dell'oggetto. La voce ACE specifica dell'oggetto per il set di proprietà 1 consente a tutti gli utenti di accedere alle proprietà A e B. L'altra voce ACE specifica dell'oggetto consente a tutti gli utenti di accedere alla proprietà C. si noti che, sebbene questo DACL non disponga di Ace con accesso negato, nega in modo implicito l'accesso alla proprietà D a tutti gli utenti tranne il gruppo A.

Quando un utente tenta di accedere alla proprietà di un oggetto, il sistema controlla le voci ACE, in ordine, fino a quando l'accesso richiesto non viene concesso o negato in modo esplicito o non ci sono più voci ACE, nel qual caso l'accesso viene negato in modo implicito.

Il sistema valuta:

-   Ace applicabili all'oggetto stesso
-   Voci ACE specifiche dell'oggetto applicabili al set di proprietà che contiene la proprietà a cui si accede
-   Voci ACE specifiche dell'oggetto applicabili alla proprietà a cui si accede

Il sistema ignora le voci ACE specifiche dell'oggetto applicabili ad altri set di proprietà o proprietà.

 

 
