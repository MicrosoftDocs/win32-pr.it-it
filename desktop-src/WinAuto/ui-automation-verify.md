---
title: Verifica automazione interfaccia utente (verifica UIA)
description: Verifica di automazione interfaccia utente (UIA Verify) è un Framework di test per test manuali e automatizzati dell'implementazione di un'applicazione o di un controllo dell'automazione interfaccia utente Microsoft.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Strumento di verifica dell'automazione interfaccia utente
- Verifica di UIA
- Implementazione di automazione interfaccia utente, test
- test di automazione interfaccia utente
- Strumenti di test di UIA
- Strumenti di test di automazione interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398660"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>Strumenti di accessibilità-verifica automazione interfaccia utente (verifica UIA)

Verifica di **automazione interfaccia utente (UIA Verify)** è un Framework di test per test manuali e automatizzati dell'implementazione di un'applicazione o di un controllo dell'automazione interfaccia utente Microsoft. La maggior parte delle funzionalità del Framework di testing deriva da una DLL denominata WUIATestLibrary.dll. Questa DLL contiene il codice per il test delle funzionalità specifiche di automazione interfaccia utente e supporta anche la registrazione dei risultati del test. È possibile integrare l'applicazione nel codice di test ed eseguire verifiche regolari e automatizzate dei test o degli scenari di automazione dell'interfaccia utente.

La **Verifica di UIA** viene installata con Windows Software Development Kit (SDK). Si trova nella \\ cartella bin \\ < *versione* > \\ <  > \\ della piattaforma UIAVerify del percorso di installazione SDK (VisualUIAVerifyNative.exe).

Il metodo di **Verifica** dell'interfaccia utente è costituito da un'API denominata libreria di test di automazione interfaccia utente e da un'interfaccia GUI denominata **Verifica di automazione interfaccia utente**. Questi argomenti sono descritti negli argomenti seguenti.

> [!NOTE]
> La **Verifica di automazione interfaccia utente** è uno strumento legacy. È invece consigliabile usare [informazioni dettagliate sull'accessibilità](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisiti

Automazione interfaccia utente deve essere presente nel sistema. Per ulteriori informazioni, vedere la sezione "requisiti" di [automazione interfaccia utente](entry-uiauto-win32.md).

La **Verifica di UIA** viene installata come parte del set complessivo di strumenti nel Windows SDK, non viene distribuita come download separato. Il Windows SDK include tutti gli strumenti correlati all'accessibilità descritti in questa sezione. [Ottenere il Windows SDK.](https://developer.microsoft.com/) È anche disponibile un archivio di download dell'SDK collegato da tale pagina, se è necessaria una versione precedente.

Per eseguire la **Verifica di UIA** come strumento visivo, trovare VisualUIAVerifyNative.exe nella \\ cartella bin \\ < *Platform* > \\ UIAVerify ed eseguirlo (in genere non è necessario eseguirlo come amministratore). Per altre informazioni, vedere [Visual UI Automation Verify](visual-ui-automation-verify.md). Per usare le librerie, vedere [libreria di test di automazione interfaccia utente](ui-automation-test-library.md).

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

 

 




