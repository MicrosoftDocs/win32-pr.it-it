---
description: SACL per un nuovo oggetto
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL per un nuovo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308139"
---
# <a name="sacl-for-a-new-object"></a>SACL per un nuovo oggetto

Il sistema utilizza l'algoritmo seguente per compilare un SACL per la maggior parte dei tipi di nuovi oggetti a protezione diretta:

1.  Il SACL dell'oggetto è l'elenco SACL del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) specificato dal creatore dell'oggetto. Il sistema unisce tutte le voci ACE ereditabili nell'elenco SACL specificato, a meno che non \_ \_ sia impostato il bit protetto di se nei bit di controllo del descrittore di sicurezza. \_Le voci \_ ACE degli attributi delle risorse di sistema \_ e \_ \_ \_ le voci ACE con ambito di sistema di \_ un oggetto padre verranno unite a un nuovo oggetto anche se \_ \_ è impostato il bit protetto se SACL.
2.  Se il creatore non specifica un descrittore di sicurezza, il sistema compila il SACL dell'oggetto da ACE ereditabili.
3.  Se non esiste alcun SACL specificato o ereditato, l'oggetto non dispone di SACL.

Per specificare un SACL per un nuovo oggetto, il creatore dell'oggetto deve avere il privilegio SE il \_ nome di sicurezza è \_ abilitato. [](privileges.md) Se il SACL specificato per un nuovo oggetto contiene solo \_ ACE attributo risorsa di sistema \_ \_ , il privilegio se il \_ nome di sicurezza \_ non è obbligatorio. Il creatore non necessita di questo privilegio se il SACL dell'oggetto viene compilato dalle voci ACE ereditate.

Il sistema utilizza un algoritmo diverso per compilare un SACL per un nuovo oggetto Active Directory. Per ulteriori informazioni, vedere [la pagina relativa alla modalità di impostazione dei descrittori di sicurezza per i nuovi oggetti directory](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
