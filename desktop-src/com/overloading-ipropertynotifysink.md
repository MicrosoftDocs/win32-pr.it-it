---
title: Overload di IPropertyNotifySink
description: Overload di IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4faca0027144498138e1a60bf3df9a29b618aeb7eb09198ff97a3dd7616be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310024"
---
# <a name="overloading-ipropertynotifysink"></a>Overload di IPropertyNotifySink

Molti ActiveX di controlli implementano una finestra di esplorazione delle proprietà non modali. Se le proprietà di un controllo vengono modificate tramite le pagine delle proprietà del controllo, le proprietà del controllo possono non essere sincronizzate con la visualizzazione del contenitore di tali proprietà (il controllo è sempre a destra, naturalmente). Per assicurarsi che abbia sempre i valori correnti per le proprietà di un controllo, un contenitore di controlli ActiveX può eseguire l'overload dell'interfaccia [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (data binding) e usarlo per ricevere una notifica che indica che una proprietà del controllo è stata modificata. Questa tecnica è facoltativa e non è necessaria per ActiveX contenitori di controlli o ActiveX personalizzati.

Si noti che un controllo deve usare [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) solo per data binding; è possibile usare [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) per uno o entrambi gli scopi.

 

 




