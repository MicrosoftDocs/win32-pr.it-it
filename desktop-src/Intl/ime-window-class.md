---
description: La classe finestra IME è una classe globale di sistema predefinita che definisce l'aspetto e il comportamento delle finestre IME standard.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Classe finestra IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56449534467a2b01ce8e59991bfc1c5f5ad4e1a9156f86cee5e154a8b8eb1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107191"
---
# <a name="ime-window-class"></a>Classe finestra IME

La classe finestra IME è una classe globale di sistema predefinita che definisce l'aspetto e il comportamento delle finestre IME standard. La classe è simile alle classi di controllo comuni in cui l'applicazione crea una finestra di questa classe usando la [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Analogamente ai controlli statici, una finestra IME non risponde di per sé all'input dell'utente. Invia invece una notifica all'IME delle azioni di input dell'utente ed elabora i messaggi di controllo inviati dall'IME o dalle applicazioni per eseguire una risposta all'azione dell'utente.

Le applicazioni con supporto IME talvolta creano finestre IME personalizzate usando la classe finestra IME. L'uso della personalizzazione della finestra consente all'applicazione di sfruttare l'elaborazione predefinita della finestra IME con il controllo del posizionamento della finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 
