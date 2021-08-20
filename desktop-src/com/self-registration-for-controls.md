---
title: Registrazione automatica per i controlli
description: Registrazione automatica per i controlli
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f7d2b07dee08657a4091d65765d35f58415ba0181088c523c02531b47f9c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918075"
---
# <a name="self-registration-for-controls"></a>Registrazione automatica per i controlli

ActiveX controlli devono supportare la registrazione automatica implementando le funzioni [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer.**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) ActiveX controlli devono registrare tutte le voci del Registro di sistema standard per gli oggetti incorporabili e i server di automazione.

ActiveX controlli devono usare l'API delle categorie di componenti per registrarsi come controllo e registrare le categorie di componenti che richiedono un host per supportare ed eventuali categorie implementate dal controllo, vedere Categorie [di componenti.](component-categories.md)

ActiveX controlli devono anche registrare la [chiave del Registro di sistema ToolBoxBitmap32,](toolboxbitmap32.md) anche se non è obbligatorio.

La categoria di componenti inseribili deve essere registrata solo se il controllo è adatto per l'uso come oggetto documento composto. È importante notare che un oggetto documento composto deve supportare alcune interfacce oltre il valore [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) minimo necessario per un ActiveX controllo. Anche se ActiveX controllo può qualificarsi come oggetto documento composto, la documentazione del controllo deve definire chiaramente il comportamento previsto in queste circostanze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli](controls.md)
</dt> </dl>

 

 