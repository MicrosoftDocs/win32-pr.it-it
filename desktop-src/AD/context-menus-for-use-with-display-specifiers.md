---
title: Menu di scelta rapida da usare con gli identificatori di visualizzazione
description: Gli snap-in di MMC di amministrazione Active Directory e la shell di Windows 2000 forniscono un meccanismo per aggiungere un elemento al menu di scelta rapida visualizzato per gli oggetti in Active Directory Domain Services.
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- Visualizza identificatori AD, menu di scelta rapida per
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fbf703f17ea5c0fa7938365d485998be77e8d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956341"
---
# <a name="context-menus-for-use-with-display-specifiers"></a>Menu di scelta rapida da usare con gli identificatori di visualizzazione

Gli snap-in di MMC di amministrazione Active Directory e la shell di Windows 2000 forniscono un meccanismo per aggiungere un elemento al menu di scelta rapida visualizzato per gli oggetti in Active Directory Domain Services. È possibile aggiungere una voce del menu di scelta rapida implementando un server COM in-process noto come *estensione del menu di scelta rapida*. È anche possibile aggiungere una voce del menu di scelta rapida che richiama qualsiasi file avviato con l'API [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , ad esempio l'URL di un'applicazione o di una pagina Web. Questa operazione è nota come *voce di menu di scelta rapida statica*.

## <a name="developer-audience"></a>Sviluppatori

In questa documentazione si presuppone che il lettore abbia familiarità con l'operazione COM e lo sviluppo di componenti con C++. Non è attualmente possibile creare un'estensione del menu di scelta rapida Active Directory Domain Services utilizzando Microsoft Visual Basic.

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a>Estensione del menu di scelta rapida con un'estensione del menu di scelta rapida

Un'estensione del menu di scelta rapida è un server COM in-process che implementa determinate interfacce e viene registrato con Active Directory Domain Services.

**Per creare e installare un'estensione del menu di scelta rapida**

1.  Creare la DLL di estensione del menu di scelta rapida. Un'estensione del menu di scelta rapida è un server COM in-process che implementa come minimo le interfacce [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Per ulteriori informazioni, vedere [implementazione dell'oggetto com del menu di scelta rapida](implementing-the-context-menu-com-object.md).
2.  Installare l'estensione della finestra del menu di scelta rapida nei computer in cui viene utilizzata l'estensione del menu di scelta rapida. Questa operazione viene eseguita creando un pacchetto di Microsoft Windows Installer per la DLL di estensione del menu di scelta rapida e distribuendo il pacchetto in modo appropriato usando i criteri di gruppo. Per ulteriori informazioni, vedere la pagina relativa alla [distribuzione dei componenti dell'interfaccia utente](distributing-user-interface-components.md).
3.  Registrare l'estensione del menu di scelta rapida nel registro di sistema di Windows e con Active Directory Domain Services. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione dell'oggetto com del menu di scelta rapida in un identificatore di visualizzazione](registering-the-context-menu-com-object-in-a-display-specifier.md).

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a>Estensione del menu di scelta rapida con una voce di menu di scelta rapida statica

Una voce di menu di scelta rapida statica può essere usata per richiamare qualsiasi file avviato con l'API [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , ad esempio l'URL di un'applicazione o di una pagina Web. A tale scopo, la voce del menu di scelta rapida statico per una determinata classe di oggetti deve essere registrata in modo che la voce di menu di scelta rapida statica venga aggiunta al menu di scelta rapida degli oggetti di tale classe. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di una voce di menu di scelta rapida statica](registering-a-static-context-menu-item.md).

 

 