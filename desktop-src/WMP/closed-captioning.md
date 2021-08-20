---
title: Sottotitoli
description: Sottotitoli
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player a oggetti, Synchronized Accessible Media Interchange (SAMI)
- modello a oggetti, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Dispositivi mobili, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player ActiveX controllo, Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Controllo ActiveX mobile,Synchronized Accessible Media Interchange (SAMI)
- ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player,migrazione di sottotitoli codificati
- Windows Media Player a oggetti, sottotitoli codificati
- modello a oggetti, migrazione di sottotitoli codificati
- Windows Media Player dispositivi mobili, migrazione di sottotitoli codificati
- Windows Media Player ActiveX, migrazione di sottotitoli codificati
- Windows Media Player Controllo ActiveX per dispositivi mobili, migrazione di sottotitoli codificati
- ActiveX, migrazione di sottotitoli codificati
- Synchronized Accessible Media Interchange (SAMI), migrazione di sottotitoli codificati
- SAMI (Synchronized Accessible Media Interchange), migrazione di sottotitoli codificati
- guida alla migrazione, Synchronized Accessible Media Interchange (SAMI)
- guida alla migrazione, sottotitoli codificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa83cb5fb6735475a883986673c958db9642386bd8ce2c76151ddd6c2f23ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119601"
---
# <a name="closed-captioning"></a>Sottotitoli

Il controllo ActiveX Windows Media Player 6.4 include un pannello di visualizzazione dei sottotitoli codificati integrato che, se reso visibile, abilita i sottotitoli in lingua sami (Synchronized Accessible Media Interchange) e visualizza il testo del sottotitolo codificato. Il Windows Media Player 7 o versione successiva consente la visualizzazione della didascalia SAMI tramite un elemento **<DIV>** HTML. Esempio:


```C++
<DIV  ID = "CCDiv"></DIV>

```



Questa tecnica offre la massima flessibilità, poiché è possibile progettare la pagina Web in modo da visualizzare i sottotitoli codificati in modo personalizzato. La visualizzazione dei sottotitoli codificati non deve più essere in una posizione fissa adiacente all'Windows Media Player utente.

Dopo aver creato un'area per visualizzare i sottotitoli codificati, usare *ClosedCaption.* **proprietà captioningID** per specificare la posizione in cui Windows Media Player esegue il rendering del testo della didascalia codificata.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



Il Windows Media Player Software Development Kit (SDK) contiene un esempio funzionante di un lettore incorporato che visualizza il testo di sottotitoli codificati. Per ottenere gli esempi dell'SDK, scaricare e installare il Windows Media Player SDK completo dal sito Web Microsoft. Per altre informazioni sui sottotitoli in lingua inglese e SAMI, vedere il sito [Web Accessibilità Microsoft.](https://www.microsoft.com/enable/)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Aggiunta di sottotitoli codificati a supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> </dl>

 

 




