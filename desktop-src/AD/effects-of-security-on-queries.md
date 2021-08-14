---
title: Effetti della sicurezza nella ricerca
description: La sicurezza è un filtro implicito quando si eseguono ricerche, enumerano contenitori o si leggono proprietà.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- effetti della sicurezza sulla ricerca in Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 429150489f2ab4d00015744beff72ee2b90b0399afd3d43f9263d39cadbaecd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191621"
---
# <a name="effects-of-security-on-searching"></a>Effetti della sicurezza nella ricerca

La sicurezza è un filtro implicito quando si eseguono ricerche, enumerano contenitori o si leggono proprietà.

ADSI può restituire errori NO SUCH PROPERTY o NO SUCH OBJECT anche quando l'oggetto esiste se non si ha accesso agli attributi di \_ \_ lettura per \_ \_ l'oggetto.

Ad esempio, un chiamante può essere in grado di enumerare gli oggetti figlio in un contenitore perché il chiamante dispone dei diritti LIST \_ CONTENTS per il contenitore. Tuttavia, lo stesso chiamante potrebbe non essere in grado di accedere agli oggetti enumerati se il chiamante non ha accesso in lettura agli oggetti figlio. In questo caso, una query per un oggetto figlio può restituire NO SUCH OBJECT anche se il chiamante ha \_ \_ enumerato correttamente l'oggetto.

Se il chiamante non dispone di diritti sufficienti, possono essere restituiti i codici restituiti seguenti:

OGGETTO \_ DOMINIO ADS \_ NON \_ \_ VALIDO

PROPRIETÀ \_ ADS \_ E NON \_ \_ SUPPORTATA

PROPRIETÀ \_ ADS \_ E NON \_ \_ TROVATA

 

 




