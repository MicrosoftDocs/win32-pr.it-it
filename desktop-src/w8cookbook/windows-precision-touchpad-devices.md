---
title: Dispositivi touchpad di precisione Windows
description: Dispositivi touchpad di precisione Windows
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07107c1d9532c4a4663a667a8e3db64124f23e5d
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "104398437"
---
# <a name="windows-precision-touchpad-devices"></a>Dispositivi touchpad di precisione Windows

## <a name="platforms"></a>Piattaforme

<dl> Client-Windows 8.1  
</dl>

## <a name="description"></a>Descrizione

Windows Precision touchpad è una nuova classe di dispositivi di input che fornisce funzionalità di input e movimento del puntatore a precisione elevata. Per impostazione predefinita, questi dispositivi generano messaggi della rotellina di scorrimento con precisione elevata per l'utilizzo delle applicazioni desktop.

## <a name="manifestations"></a>Manifestazioni

Le applicazioni che non sono progettate per gestire i messaggi della rotellina di scorrimento con precisione ultra-alta possono scorrere in modo non corretto.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Gli sviluppatori di applicazioni devono esaminare il Delta di scorrimento nei messaggi della rotellina di scorrimento del mouse e modificare le proprie app di conseguenza. Tuttavia, nel frattempo un'applicazione può rifiutare esplicitamente i messaggi della rotellina di scorrimento con precisione elevatissima (Delta = 1) e scegliere di ricevere messaggi della rotellina di scorrimento ad alta precisione (Delta = 40) o messaggi della rotellina di scorrimento standard (Delta = 120).

## <a name="solution"></a>Soluzione

Se l'applicazione è in grado di gestire i messaggi della rotellina di scorrimento con precisione elevatissima, non è necessario eseguire alcuna operazione perché questo è il messaggio predefinito inviato da touchpad di precisione di Windows.

Se l'applicazione è in grado di gestire i messaggi della rotellina di scorrimento a precisione elevata, ma non i messaggi della rotellina con precisione elevata, aggiungere quanto segue al manifesto dell'applicazione:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



Se l'applicazione non è in grado di gestire i messaggi della rotellina di scorrimento a precisione elevata o i messaggi della rotellina con precisione elevata, aggiungere il codice seguente al manifesto dell'applicazione per indicare che si desiderano i messaggi della rotellina di scorrimento standard:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




