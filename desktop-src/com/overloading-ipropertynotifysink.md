---
title: Overload di IPropertyNotifySink
description: Overload di IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396646"
---
# <a name="overloading-ipropertynotifysink"></a>Overload di IPropertyNotifySink

Molti contenitori di controlli ActiveX implementano una finestra di esplorazione delle proprietà non modale. Se le proprietà di un controllo vengono modificate tramite le pagine delle proprietà del controllo, le proprietà del controllo possono non essere sincronizzate con la visualizzazione del contenitore di tali proprietà (ovviamente, il controllo è sempre a destra). Per assicurarsi che disponga sempre dei valori correnti per le proprietà di un controllo, un contenitore di controlli ActiveX può sovraccaricare l'interfaccia [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (Data Binding) e utilizzarla anche per ricevere una notifica della modifica di una proprietà del controllo. Questa tecnica è facoltativa e non è necessaria per i contenitori di controlli ActiveX o i controlli ActiveX.

Si noti che un controllo deve usare [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) solo per data binding; è possibile utilizzare [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) per uno o entrambi gli scopi.

 

 




