---
description: Windows Sockets 1.1 ha introdotto il meccanismo async-select per fornire indicazioni di eventi di rete che non comportano il polling o il blocco.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Windows Messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bab33ecb4d2898c8f1e363ab19ad425503e9d005bf24229a29f581aadf1788f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993211"
---
# <a name="windows-messages"></a>Windows Messaggi

Windows Sockets 1.1 ha introdotto il meccanismo async-select per fornire indicazioni di eventi di rete che non comportano il polling o il blocco. La [**funzione WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) viene usata per registrare un interesse per uno o più eventi di rete come elencato in precedenza e fornire un handle di finestra da usare per la notifica. Quando si verifica un evento di rete designato, un messaggio di Windows specificato dal client viene inviato alla finestra indicata. A tale scopo, il provider di servizi deve usare la funzione [**WPUPostMessage.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage)

In Windows, questo potrebbe non essere il meccanismo di notifica più efficiente ed è poco pratico per i daemon e i servizi che non vogliono aprire alcuna finestra. Per risolvere questo problema, è stato introdotto il meccanismo di segnalazione degli oggetti evento descritto di seguito.

 

 
