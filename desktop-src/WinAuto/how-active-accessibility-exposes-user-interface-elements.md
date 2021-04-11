---
title: Come Active Accessibility espone gli elementi dell'interfaccia utente
description: Microsoft Active Accessibility crea un oggetto proxy per ogni elemento dell'interfaccia utente esposto.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221417"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a>Come Active Accessibility espone gli elementi dell'interfaccia utente

Microsoft Active Accessibility crea un oggetto *proxy* per ogni elemento dell'interfaccia utente esposto. Un oggetto proxy funge da intermediario tra l'utilità client e l'elemento dell'interfaccia utente. Lo scopo dell'oggetto proxy consiste nel monitorare il ciclo di vita dell'elemento dell'interfaccia utente e implementare le proprietà e i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per conto dell'elemento dell'interfaccia utente. Gli sviluppatori di server che creano controlli personalizzati o altri elementi dell'interfaccia utente personalizzati devono anche creare oggetti proxy. Per ulteriori informazioni, vedere [creazione di oggetti proxy](creating-proxy-objects.md).

Quando Microsoft Active Accessibility crea un oggetto per esporre un controllo comune o predefinito, crea effettivamente almeno due oggetti: uno per il controllo e uno per la finestra che racchiude il controllo. Nella maggior parte dei casi, queste finestre padre hanno la [Proprietà Role](role-property.md) della [**\_ \_ finestra del sistema dei ruoli**](object-roles.md) e hanno la stessa [proprietà Name](name-property.md) e il nome della classe di finestra del controllo. Le informazioni sul controllo che i client comunicano agli utenti finali sono contenute nell'oggetto creato da Microsoft Active Accessibility per esporre il controllo, non l'oggetto padre che espone la finestra che racchiude il controllo.

Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Selezione di oggetti non necessari](screening-out-unnecessary-objects.md)
-   [Specifica della proprietà Name](providing-the-name-property.md)
-   [Verifica della corretta denominazione degli elementi dell'interfaccia utente](ensure-that-ui-elements-are-named-correctly.md)
-   [Elementi dell'interfaccia utente non supportati](unsupported-user-interface-elements.md)

 

 




