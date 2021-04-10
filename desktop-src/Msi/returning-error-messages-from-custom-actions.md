---
description: In questa sezione viene descritto come inviare messaggi da azioni personalizzate che eseguono effettivamente una parte dell'installazione chiamando una libreria a collegamento dinamico o uno script.
ms.assetid: 637efccf-920d-421d-9183-528cc3515bf8
title: Restituzione di messaggi di errore da azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480a9e7891680aadc9d8eb4eedba2bad0d2e3dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130670"
---
# <a name="returning-error-messages-from-custom-actions"></a>Restituzione di messaggi di errore da azioni personalizzate

In questa sezione viene descritto come inviare messaggi da azioni personalizzate che eseguono effettivamente una parte dell'installazione chiamando una libreria a collegamento dinamico o uno script. Si noti che il [tipo di azione personalizzata 19](custom-action-type-19.md) Invia solo un messaggio di errore specificato, restituisce un errore e quindi termina l'installazione. Il tipo di azione personalizzata 19 non esegue alcuna parte dell'installazione.

Per inviare un messaggio di errore da un'azione personalizzata che usa una [libreria di collegamento dinamico](dynamic-link-libraries.md) (dll), fare in modo che l'azione personalizzata chiami [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). Si noti che le azioni personalizzate avviate da un [ControlEvent DoAction](doaction-controlevent.md) possono inviare messaggi con il metodo del [**messaggio**](session-message.md) , ma non possono inviare un messaggio con **MsiProcessMessage**. Nei sistemi precedenti a Windows Server 2003, le azioni personalizzate avviate da un DoAction ControlEvent non possono inviare messaggi con **MsiProcessMessage** o metodo **Message** . Per altre informazioni, vedere [invio di messaggi a Windows Installer con MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

**Per visualizzare un messaggio di errore all'interno di un'azione personalizzata utilizzando una DLL**

1.  L'azione personalizzata deve chiamare [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e passare i parametri *hinstall*, *eMessageType* e *hRecord*. L'handle per l'installazione, [tipo di azione personalizzata 19](custom-action-type-19.md), può essere fornito all'azione personalizzata come descritto in [accesso alla sessione del programma di installazione corrente dall'interno di un'azione personalizzata](accessing-the-current-installer-session-from-inside-a-custom-action.md) o da [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) o [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea).
2.  Il parametro *eMessageType* deve specificare uno dei tipi di messaggio elencati in [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).
3.  Il parametro *hRecord* della funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) dipende dal tipo di messaggio. Vedere [invio di messaggi a Windows Installer con MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md). Se il messaggio contiene dati formattati, immettere il messaggio nella tabella degli [errori](error-table.md) usando la formattazione descritta in [formattato](formatted.md).

Per inviare un messaggio di errore da un'azione personalizzata che utilizza gli [script](scripts.md), l'azione personalizzata può chiamare il metodo [**Message**](session-message.md) dell'oggetto [**Session**](session-object.md) .

**Per visualizzare un messaggio di errore all'interno di un'azione personalizzata tramite script**

1.  L'azione personalizzata deve chiamare il metodo del [**messaggio**](session-message.md) dell'oggetto [**sessione**](session-object.md) e passare il *tipo* e il *record* dei parametri.
2.  Il *tipo* di parametro deve specificare uno dei tipi di messaggio elencati nel metodo del [**messaggio**](session-message.md) .
3.  Il parametro *record* del metodo del [**messaggio**](session-message.md) dipende dal tipo di messaggio. Se il messaggio contiene dati formattati, immettere il messaggio nella tabella degli [errori](error-table.md) usando la formattazione descritta in [formattato](formatted.md).

Le azioni personalizzate che usano [file eseguibili](executable-files.md) non possono inviare un messaggio chiamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) o il metodo [**Message**](session-message.md) perché non possono ottenere un handle per l'installazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Valori restituiti dell'azione personalizzata](custom-action-return-values.md)
</dt> </dl>

 

 



