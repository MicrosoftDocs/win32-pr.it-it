---
title: Debug di un'estensione Active Directory
description: La finestra delle proprietà del servizio Microsoft Active Directory directory, il menu di scelta rapida e le estensioni della creazione guidata oggetto illustrate in questo argomento sono implementate come server COM in-process.
ms.assetid: 8c280084-fd2f-4d34-a119-d4e925a68a5c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8d9646f4ccc2e8c740a81ddb48422881744f5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046530"
---
# <a name="debugging-an-active-directory-extension"></a>Debug di un'estensione Active Directory

La finestra delle proprietà del servizio Microsoft Active Directory directory, il menu di scelta rapida e le estensioni della creazione guidata oggetto illustrate in questo argomento sono implementate come server COM in-process. Ovvero ogni estensione è una DLL che viene eseguita nel contesto del processo host. Per eseguire il debug dell'estensione, è necessario associare l'estensione a un'applicazione ed eseguire l'applicazione in un debugger.

## <a name="debugging-active-directory-extensions-displayed-in-the-windows-shell"></a>Debug di estensioni Active Directory visualizzate nella shell di Windows

Le estensioni Active Directory visualizzate nella shell di Windows vengono caricate nel contesto del processo di Explorer.exe. È possibile eseguire il debug di queste estensioni come un'estensione della shell standard. Per ulteriori informazioni sul debug delle estensioni della shell, vedere [debug con la shell](/previous-versions/windows/desktop/legacy/cc144064(v=vs.85)).

## <a name="debugging-active-directory-extensions-displayed-in-the-active-directory-mmc-snap-ins"></a>Debug di estensioni Active Directory visualizzate nella Active Directory MMC Snap-Ins

Active Directory estensioni visualizzate nell'Active Directory snap-in MMC amministrativi vengono caricati nel contesto di Microsoft Management Console. Per eseguire il debug di un'estensione, individuare Mmc.exe nel sistema locale e impostare il debugger per utilizzarlo come applicazione per il debug. Nella maggior parte dei sistemi, Mmc.exe si trova nella directory di sistema di Windows, ad esempio C: \\ WinNT \\ system32. A seconda del debugger, è possibile che non sia necessario impostare la DLL di estensione in modo che venga caricata anche dal debugger. Molti debugger consentono inoltre di aggiungere il debugger a un processo MMC in esecuzione. Per ulteriori informazioni, vedere il manuale dell'utente del debugger.

Può essere utile fare in modo che MMC carichi automaticamente uno snap-in specifico. A tale scopo, impostare gli argomenti dell'applicazione sul percorso e il nome file di un file MSC. Può trattarsi di un file MSC installato dal sistema o di uno creato dall'utente. È possibile creare un file MSC attenendosi alla seguente procedura.

1.  Eseguire Mmc.exe.
2.  Caricare lo snap-in desiderato selezionando **file**  -  **Aggiungi/Rimuovi snap-in...** dal menu MMC e selezionando lo snap-in desiderato.
3.  Salvare il file msc selezionando **file**  -  **Salva con nome** dal menu MMC.

Se non si imposta un file MSC di avvio, è necessario caricare manualmente lo snap-in quando si esegue l'applicazione nel debugger.

Quando l'applicazione host viene eseguita nel debugger, il debugger può visualizzare un messaggio di avviso che informa che l'applicazione in esecuzione non contiene alcun simbolo di debug. Questo comportamento è previsto e può essere ignorato perché si esegue effettivamente il debug della DLL, non dell'applicazione host.

Nella maggior parte dei casi, l'estensione non verrà chiamata fino a quando l'utente non esegue un'azione che causa il caricamento e l'inizializzazione dell'estensione. Se, ad esempio, si esegue il debug di un'estensione del menu di scelta rapida visualizzata per gli oggetti utente, l'estensione non verrà caricata finché non viene visualizzata la prima volta il menu di scelta rapida per un oggetto utente.

A questo punto dovrebbe essere possibile impostare i punti di interruzione e visualizzare l'output di debug. Se l'estensione non sembra carica, impostare un punto di interruzione nella funzione [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) dell'estensione. Se **DllGetClassObject** non viene chiamato, è probabile che l'estensione non sia registrata correttamente.

Al termine del debug, uscire da MMC e il debugger dovrebbe scaricarlo normalmente.

 

 