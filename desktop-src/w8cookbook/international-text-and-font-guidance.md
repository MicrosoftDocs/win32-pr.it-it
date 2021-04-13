---
title: Linee guida per testo e carattere internazionali
description: Linee guida per testo e carattere internazionali
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399043"
---
# <a name="international-text-and-font-guidance"></a>Linee guida per testo e carattere internazionali

## <a name="affected-platforms"></a>Piattaforme interessate

<dl> Client-Windows 8 \| Windows 8.1  
Server-Windows Server 2012 \| Windows server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

Dal momento precedente a Windows 2000, è stato aggiunto il supporto per la visualizzazione di testo per i nuovi script in ogni versione principale di Windows. Per informazioni sulle modifiche apportate in ogni versione principale, vedere l'articolo [relativo al supporto dello script e dei tipi di carattere per Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) in [go Global Development Center](https://msdn.microsoft.com/goglobal/default).

Si noti che il supporto per uno script può richiedere alcune modifiche ai componenti dello stack di testo e alle modifiche ai tipi di carattere. Il sistema operativo Windows include molti componenti dello stack di testo: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 e altri. Le informazioni fornite riguardano principalmente GDI e DirectWrite. È inoltre generalmente applicabile ai Framework dell'interfaccia utente, ad esempio RichEdit o l'agente di rendering MSHTML usato per le app di Windows 8 Store e per il rendering del contenuto Web, sebbene tali componenti possano presentare alcune differenze.

## <a name="best-practices"></a>Procedure consigliate

**Linee guida per le tipografie per sviluppatori**

Tipografia è alla base del linguaggio di progettazione Microsoft. Ognuno dei principi di progettazione Microsoft rafforza l'importanza della tipografia. Per la prima volta, gli sviluppatori di app hanno un set di Framework che supportano funzionalità tipografiche avanzate. Per informazioni su come usare JavaScript e HTML per visualizzare e modificare il testo nelle app di Windows Store, vedere [visualizzazione e modifica del testo](/previous-versions/windows/apps/hh465442(v=win.10)) .

**Metriche dei tipi di carattere**

Le metriche dei tipi di carattere sono un'area di particolare importanza per gli sviluppatori di applicazioni. I file del tipo di carattere contengono diversi valori correlati alle metriche verticali e orizzontali. Questi valori sono documentati nella [specifica OpenType](https://www.microsoft.com/typography/otspec/) e vengono esposti tramite un'ampia gamma di API trovate nella [ \_ struttura di \_ metrica del tipo di carattere DWrite](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) e nella [struttura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

## <a name="resources"></a>Risorse

-   [Supporto dello script e dei tipi di carattere per Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Vai al centro per sviluppatori globali](https://msdn.microsoft.com/goglobal/default)
-   [Visualizzazione e modifica di testo](/previous-versions/windows/apps/hh465442(v=win.10))
-   [Specifica OpenType](https://www.microsoft.com/typography/otspec/)
-   [\_Struttura della metrica del tipo di carattere DWrite \_](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [Struttura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 