---
title: Oggetti accessibili
description: Con Microsoft Active Accessibility, gli elementi dell'interfaccia utente vengono esposti ai client come oggetti Component Object Model (COM).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9591c4884826ba9d85192e5702d0528f25087797faf83d83314d5c00f172459b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994381"
---
# <a name="accessible-objects"></a>Oggetti accessibili

Con Microsoft Active Accessibility, gli elementi dell'interfaccia utente vengono esposti ai client come oggetti Component Object Model (COM). Questi *oggetti accessibili* gestiscono informazioni, denominate proprietà , che descrivono il nome dell'oggetto, la posizione dello schermo e altre informazioni necessarie per gli strumenti di accessibilità.  Gli oggetti accessibili forniscono anche *metodi che* i client chiamano per fare in modo che l'oggetto esee attivi un'azione. Gli oggetti accessibili a cui sono associati elementi semplici sono detti *anche elementi padre* o *contenitori*.

Gli oggetti accessibili vengono implementati Microsoft Active Accessibility'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) basata su COM. I **metodi e le proprietà IAccessible** consentono alle applicazioni client di ottenere informazioni sugli elementi dell'interfaccia utente necessari agli utenti. Ad esempio, [**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) restituisce un puntatore di interfaccia all'elemento padre di un oggetto accessibile e [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) fornisce ai client un mezzo per ottenere informazioni su altri oggetti all'interno di un contenitore.

Per altre informazioni sulla relazione tra oggetti accessibili ed elementi semplici, vedere [Elementi semplici.](simple-elements.md)

 

 




