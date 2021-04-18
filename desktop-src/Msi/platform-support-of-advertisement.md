---
description: Il Windows Installer supporta l'annuncio di applicazioni e funzionalità.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Supporto della piattaforma per gli annunci
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320848"
---
# <a name="platform-support-of-advertisement"></a>Supporto della piattaforma per gli annunci

Il Windows Installer supporta l'annuncio di applicazioni e funzionalità.

Le funzionalità di annuncio seguenti sono disponibili in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP e Windows 2000.

-   Collegamenti e relative icone.

-   Le estensioni e le rispettive icone specificate nella [tabella ProgId](progid-table.md).

-   Verbi della shell e del comando registrati sotto la chiave ProgId.

-   Contesti CLSID e InProcHandler.

-   L'installazione su richiesta tramite OLE è disponibile solo a livello di codice tramite [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) e la funzione **CreateObject (Visual Basic)** o la **funzione GetObject (Visual Basic)**.

> [!Note]
> Le informazioni su AppId e TypeLib vengono scritte solo quando viene installato un componente annunciato.
> 
> Per supportare le estensioni di file, l'applicazione deve essere pubblicata per Active Directory da un amministratore che usa Criteri di gruppo.

## <a name="remarks"></a>Commenti

Per l'installazione del prodotto potrebbe non essere necessario un riavvio, ma tutti i tasti di scelta rapida annunciati non funzioneranno finché il computer non verrà riavviato. I collegamenti annunciati per le installazioni successive funzionano senza riavvio.

Per assicurarsi che i collegamenti annunciati funzionino correttamente, l'autore del pacchetto deve pianificare un riavvio forzato alla fine dell'installazione.

Per evitare riavvii superflui del sistema, pianificare l'esecuzione di un riavvio solo se non è installata alcuna versione del Windows Installer.

Le istruzioni condizionali possono controllare la proprietà [**ShellAdvtSupport**](shelladvtsupport.md) e la proprietà [**Version9X**](version9x.md) . Per ulteriori informazioni sulla pianificazione di un riavvio forzato condizionale, vedere [riavvii del sistema](system-reboots.md) e [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).

 

 
