---
title: Oggetti accessibili
description: Con Microsoft Active Accessibility, gli elementi dell'interfaccia utente vengono esposti ai client come oggetti Component Object Model (COM).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396815"
---
# <a name="accessible-objects"></a>Oggetti accessibili

Con Microsoft Active Accessibility, gli elementi dell'interfaccia utente vengono esposti ai client come oggetti Component Object Model (COM). Questi *oggetti accessibili* gestiscono informazioni, denominate *Proprietà*, che descrivono il nome dell'oggetto, la posizione dello schermo e altre informazioni necessarie per gli strumenti di accessibilità. Gli oggetti accessibili forniscono anche *Metodi* che i client chiamano per provocare l'esecuzione di un'azione da parte dell'oggetto. Gli oggetti accessibili a cui sono associati elementi semplici sono denominati anche elementi *padre* o *contenitori*.

Gli oggetti accessibili vengono implementati utilizzando l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) basata su com di Microsoft Active Accessibility. I metodi e le proprietà **IAccessible** consentono alle applicazioni client di ottenere informazioni sugli elementi dell'interfaccia utente necessari per gli utenti. Ad esempio, [**IAccessible:: Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) restituisce un puntatore di interfaccia all'elemento padre di un oggetto accessibile e [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) consente ai client di ottenere informazioni su altri oggetti all'interno di un contenitore.

Per ulteriori informazioni sulla correlazione tra oggetti accessibili ed elementi semplici, vedere [elementi semplici](simple-elements.md).

 

 




