---
description: Uso dei menu creati dal proprietario per supportare la funzionalità di riconoscimento vocale per il Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Uso di menu Owner-Drawn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751271"
---
# <a name="using-owner-drawn-menus"></a>Uso di menu Owner-Drawn

Quando si usano i menu creati dal proprietario, è necessario rendere disponibili i nomi di menu per supportare la funzionalità di riconoscimento vocale. A questo scopo è possibile procedere in due modi:

-   Esporre il nome della voce di menu utilizzando la struttura MSAAMENUINFO.
-   Consente di sostituire i menu grafici con i menu di testo standard quando è attivo un supporto per l'accessibilità. Se la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) restituisce **true** con il relativo parametro *uiAction* impostato su SPI \_ GETSCREENREADER, usare i menu standard. L'applicazione deve controllare il messaggio WM \_ SETTINGSCHANGE e rispondere eseguendo una query sullo stato di questa opzione e modificando in modo appropriato la visualizzazione. Microsoft Visual Studio, ad esempio, offre un'opzione per utilizzare i menu standard anziché i menu personalizzati visualizzati per impostazione predefinita.

 

 
