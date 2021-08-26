---
title: Windows touchpad di precisione
description: Windows touchpad di precisione
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb81978c9c9849dfa0d073a4b37af3760d1d4e5bc8e8fa2e81317293db04fc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007901"
---
# <a name="windows-precision-touchpad-devices"></a>Windows touchpad di precisione

## <a name="platforms"></a>Piattaforme

<dl> Client - Windows 8.1  
</dl>

## <a name="description"></a>Descrizione

Il Windows Touchpad di precisione è una nuova classe di dispositivi di input che forniscono funzionalità di input e movimento del puntatore ad alta precisione. Per impostazione predefinita, questi dispositivi generano messaggi con rotellina di scorrimento ad alta precisione per l'utilizzo di applicazioni desktop.

## <a name="manifestations"></a>Manifestazioni

Le applicazioni che non sono progettate per gestire i messaggi della rotellina di scorrimento ad alta precisione possono scorrere o non scorrere correttamente.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Gli sviluppatori di applicazioni devono esaminare il delta di scorrimento nei messaggi della rotellina del mouse e modificare le app di conseguenza. Tuttavia, nel frattempo un'applicazione può rifiutare esplicitamente i messaggi della rotellina di scorrimento ad alta precisione (delta = 1) e scegliere di ricevere messaggi con rotellina di scorrimento ad alta precisione (delta = 40) o messaggi con rotellina di scorrimento standard (delta = 120).

## <a name="solution"></a>Soluzione

Se l'applicazione è in grado di gestire i messaggi della rotellina di scorrimento ad alta precisione, non è necessario eseguire alcuna operazione perché si tratta del messaggio predefinito inviato da Windows Touchpad di precisione.

Se l'applicazione è in grado di gestire i messaggi della rotellina di scorrimento ad alta precisione, ma non i messaggi relativi alla rotellina ad alta precisione, aggiungere quanto segue al manifesto dell'applicazione:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



Se l'applicazione non è in grado di gestire i messaggi della rotellina di scorrimento ad alta precisione o i messaggi della rotellina ad alta precisione, aggiungere quanto segue al manifesto dell'applicazione per indicare che sono desiderati i messaggi standard della rotellina di scorrimento:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




