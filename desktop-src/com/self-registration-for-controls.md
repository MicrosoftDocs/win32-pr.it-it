---
title: Registrazione automatica per i controlli
description: Registrazione automatica per i controlli
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300528"
---
# <a name="self-registration-for-controls"></a>Registrazione automatica per i controlli

I controlli ActiveX devono supportare la registrazione automatica mediante l'implementazione delle funzioni [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) . I controlli ActiveX devono registrare tutte le voci del registro di sistema standard per gli oggetti incorporabili e i server di automazione.

I controlli ActiveX devono usare l'API delle categorie di componenti per registrarsi come controllo e registrare le categorie di componenti che richiedono un host per supportare e tutte le categorie implementate dal controllo, vedere [categorie di componenti](component-categories.md).

Anche i controlli ActiveX devono registrare la chiave del registro di sistema [ToolboxBitmap32](toolboxbitmap32.md) , anche se questa operazione non è obbligatoria.

La categoria di componenti inseribili deve essere registrata solo se il controllo è adatto per essere utilizzato come oggetto documento composto. È importante notare che un oggetto documento composto deve supportare determinate interfacce oltre il numero minimo di [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) necessario per un controllo ActiveX. Sebbene un controllo ActiveX possa essere qualificato come oggetto documento composto, la documentazione del controllo deve indicare chiaramente il comportamento previsto in tali circostanze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli](controls.md)
</dt> </dl>

 

 