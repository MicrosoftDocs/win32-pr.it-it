---
title: Automazione interfaccia utente verifica (verifica dell'interfaccia utente)
description: Automazione interfaccia utente Verify (UIA Verify) è un framework di test per il test manuale e automatizzato dell'implementazione di Microsoft Automazione interfaccia utente di un controllo o di un'applicazione.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Strumento di verifica dell'automazione interfaccia utente
- Verifica dell'interfaccia utente
- Automazione interfaccia utente, test
- test Automazione interfaccia utente
- Strumenti di test dell'interfaccia utente
- Automazione interfaccia utente strumenti di test
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f8c97d6522e353445ededff47a9a7cf123998b94f1323f1df59b7a380ac1d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052389"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>Strumenti di accessibilità - Verifica Automazione interfaccia utente (verifica dell'interfaccia utente)

**Automazione interfaccia utente Verify (UIA Verify)** è un framework di test per il test manuale e automatizzato dell'implementazione di Microsoft Automazione interfaccia utente di un controllo o di un'applicazione. La maggior parte delle funzionalità del framework di test proviene da una DLL denominata WUIATestLibrary.dll. Questa DLL contiene il codice per il test di Automazione interfaccia utente funzionalità specifiche e supporta anche la registrazione dei risultati del test. È possibile integrare l'applicazione nel codice di test ed eseguire normali test automatizzati o controlli spot Automazione interfaccia utente scenari.

**UiA Verify** viene installato con Windows Software Development Kit (SDK). Si trova nella cartella UIAVerify della piattaforma della versione bin del percorso di installazione \\ \\ <  > \\ <  > \\ dell'SDK (VisualUIAVerifyNative.exe).

**UiA Verify** è costituito da un'API denominata Automazione interfaccia utente Test Library e da un'interfaccia gui denominata Visual **Automazione interfaccia utente Verify**. Questi argomenti sono descritti negli argomenti seguenti.

> [!NOTE]
> **Automazione interfaccia utente Verify** è uno strumento legacy. In alternativa, è [consigliabile Insights](https://accessibilityinsights.io/) accessibilità.

## <a name="requirements"></a>Requisiti

Automazione interfaccia utente deve essere presente nel sistema. Per altre informazioni, vedere la sezione "Requisiti" di [Automazione interfaccia utente](entry-uiauto-win32.md).

**UiA Verify** viene installato come parte del set complessivo di strumenti in Windows SDK, non viene distribuito come download separato. L Windows SDK include tutti gli strumenti correlati all'accessibilità documentati in questa sezione. [Ottenere l Windows SDK.](https://developer.microsoft.com/) È anche disponibile un archivio di download dell'SDK collegato da tale pagina, se è necessaria una versione precedente.

Per eseguire **UIA Verify** come strumento visivo, trovare VisualUIAVerifyNative.exe nella cartella \\ \\ <  > \\ UIAVerify della piattaforma bin ed eseguirla (in genere non è necessario eseguire come amministratore). Per altre informazioni, vedere [Visual Automazione interfaccia utente Verify](visual-ui-automation-verify.md). Per usare le librerie, vedere Automazione interfaccia utente [Test Library](ui-automation-test-library.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accessible Event Watcher](accessible-event-watcher.md)
</dt> <dt>

[Controllare](inspect-objects.md)
</dt> <dt>

[Strumenti di test](testing-tools.md)
</dt> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 




