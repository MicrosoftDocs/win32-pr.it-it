---
description: Stringa agente utente
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Stringa agente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a4d918845fe317ef64569cde7ef79c7bb1461bcd0205a5ef74daf55b2c0186
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328697"
---
# <a name="user-agent-string"></a>Stringa agente utente

La *stringa agente utente* contiene informazioni sull'identità di un browser. La stringa agente utente viene segnalata al server Web come intestazione HTTP ogni volta che un browser effettua una richiesta a un server Web. È anche possibile accedervi tramite uno script sul lato client. Ad esempio, è possibile visualizzare la stringa agente utente digitando l'URL seguente nella barra degli indirizzi Windows Internet Explorer 8: "javascript:alert(navigator.userAgent)". La figura seguente mostra la tipica finestra di dialogo risultante Internet Explorer 8 in esecuzione Windows 7.

![Screenshot della casella del diaog di Internet Explorer con la stringa dell'agente utente](images/useragent-alert.png)

In genere, la stringa dell'agente utente viene analizzata in modo specifico per la sottostringa MSIE. In base alla versione segnalata del browser, la logica di programmazione lato client o lato server richiede un'azione diversa. Per altre informazioni sulla stringa agente utente, vedere What [Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in MSDN Library.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



