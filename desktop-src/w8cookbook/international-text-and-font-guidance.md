---
title: Linee guida internazionali per testo e tipi di carattere
description: Linee guida internazionali per testo e tipi di carattere
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76eeeeaf59f777610603787c3b8e6ed248f36810d34fc2026466b72ca57a1883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935401"
---
# <a name="international-text-and-font-guidance"></a>Linee guida internazionali per testo e tipi di carattere

## <a name="affected-platforms"></a>Piattaforme interessate

<dl> Client - Windows 8 \| Windows 8.1  
Server - Windows Server 2012 \| Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

A partire Windows 2000, il supporto per la visualizzazione del testo per i nuovi script è stato aggiunto in ogni versione principale di Windows. Le descrizioni delle modifiche apportate in ogni versione principale sono disponibili nell'articolo [Supporto](https://msdn.microsoft.com/goglobal/bb688099.aspx) di script e tipi di carattere per Windows nel [Go Global Development Center.](https://msdn.microsoft.com/goglobal/default)

Si noti che il supporto per uno script può richiedere determinate modifiche ai componenti dello stack di testo, nonché modifiche ai tipi di carattere. Il Windows operativo include molti componenti dello stack di testo: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 e altri. Le informazioni fornite riguardano principalmente GDI e DirectWrite. È applicabile anche ai framework dell'interfaccia utente, ad esempio RichEdit o l'agente di rendering MSHTML usato per le app di Windows 8 Store e per il rendering di contenuto Web, anche se questi componenti possono presentare alcune differenze.

## <a name="best-practices"></a>Procedure consigliate

**Indicazioni tipografiche per gli sviluppatori**

La tipografia è alla base del linguaggio di progettazione Microsoft. Ognuno dei principi di progettazione Microsoft rafforza l'importanza della tipografia. Per la prima volta, gli sviluppatori di app hanno un set di framework che supportano funzionalità tipografiche avanzate. Passare a [Visualizzazione e modifica del testo](/previous-versions/windows/apps/hh465442(v=win.10)) per informazioni su come usare JavaScript e HTML per visualizzare e modificare il testo nelle app Windows Store.

**Metriche dei tipi di carattere**

Le metriche dei tipi di carattere sono un'area di particolare importanza per gli sviluppatori di applicazioni. I file dei tipi di carattere contengono vari valori correlati alle metriche verticali e orizzontali. Questi valori sono documentati nella specifica [OpenType](https://www.microsoft.com/typography/otspec/) e vengono esposti tramite un'ampia gamma di API disponibili nella struttura [DWRITE \_ FONT \_ METRICS](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) e in [TEXTMETRIC Structure](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

## <a name="resources"></a>Risorse

-   [Supporto di script e tipi di carattere per Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Go Global Development Center](https://msdn.microsoft.com/goglobal/default)
-   [Visualizzazione e modifica del testo](/previous-versions/windows/apps/hh465442(v=win.10))
-   [Specifica OpenType](https://www.microsoft.com/typography/otspec/)
-   [Struttura DWRITE \_ FONT \_ METRICS](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [Struttura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 