---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Stringa agente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968741"
---
# <a name="user-agent-string"></a>Stringa agente utente

La *stringa agente utente* contiene informazioni sull'identità di un browser. La stringa agente utente viene segnalata al server Web come intestazione HTTP ogni volta che un browser esegue una richiesta a un server Web. È anche possibile accedervi tramite uno script sul lato client. Ad esempio, è possibile visualizzare la stringa agente utente digitando l'URL seguente nella barra degli indirizzi di Windows Internet Explorer 8: "JavaScript: Alert (Navigator. userAgent)". Nell'illustrazione seguente viene mostrata la finestra di dialogo tipica risultante da Internet Explorer 8 in esecuzione in Windows 7.

![screenshot della finestra di Internet Explorer diaog con la stringa agente utente](images/useragent-alert.png)

In genere, la stringa agente utente viene analizzata in modo specifico per la sottostringa MSIE. In base alla versione segnalata del browser, la logica di programmazione lato client o lato server esegue un'azione diversa. Per ulteriori informazioni sulla stringa agente utente, vedere [quali sono i report di Windows Internet Explorer come stringa di User-Agent?](/previous-versions/cc817582(v=msdn.10)) in MSDN Library.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



