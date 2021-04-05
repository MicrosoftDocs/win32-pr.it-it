---
description: La classe della finestra IME è una classe globale di sistema predefinita che definisce l'aspetto e il comportamento delle finestre IME standard.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Classe della finestra IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882145"
---
# <a name="ime-window-class"></a>Classe della finestra IME

La classe della finestra IME è una classe globale di sistema predefinita che definisce l'aspetto e il comportamento delle finestre IME standard. La classe è simile alle classi di controlli comuni in quanto l'applicazione crea una finestra di questa classe tramite la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Analogamente ai controlli statici, una finestra IME non risponde all'input dell'utente. Al contrario, notifica all'IME le azioni di input dell'utente ed elabora i messaggi di controllo inviati dall'IME o dalle applicazioni per eseguire una risposta all'azione dell'utente.

Le applicazioni compatibili con IME talvolta creano finestre IME personalizzate utilizzando la classe della finestra IME. L'utilizzo della personalizzazione della finestra consente all'applicazione di sfruttare i vantaggi dell'elaborazione predefinita della finestra IME con il controllo del posizionamento della finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 
