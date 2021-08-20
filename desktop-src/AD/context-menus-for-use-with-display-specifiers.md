---
title: Menu di scelta rapida da usare con gli identificatori di visualizzazione
description: Gli snap-in mmc amministrativi di Active Directory e la shell di Windows 2000 forniscono un meccanismo per aggiungere un elemento al menu di scelta rapida visualizzato per gli oggetti in Active Directory Domain Services.
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- identificatori di visualizzazione AD, menu di scelta rapida per
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b55b530797f1ac43456606d0fecf30e7641bf10399fb3c074135a3e0c49fd0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021708"
---
# <a name="context-menus-for-use-with-display-specifiers"></a>Menu di scelta rapida da usare con gli identificatori di visualizzazione

Gli snap-in mmc amministrativi di Active Directory e la shell di Windows 2000 forniscono un meccanismo per aggiungere un elemento al menu di scelta rapida visualizzato per gli oggetti in Active Directory Domain Services. È possibile aggiungere una voce di menu di scelta rapida implementando un server COM in-process noto come estensione *del menu di scelta rapida*. È anche possibile aggiungere una voce di menu di scelta rapida che richiama qualsiasi file avviato con l'API [**ShellExecute,**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) ad esempio un URL di applicazione o di pagina Web. Questa operazione è nota come voce *di menu di scelta rapida statica.*

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione presuppone che il lettore abbia familiarità con le operazioni COM e lo sviluppo di componenti con C++. Attualmente non è possibile creare un'estensione Active Directory Domain Services menu di scelta rapida usando Microsoft Visual Basic.

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a>Estensione del menu di scelta rapida con un'estensione del menu di scelta rapida

Un'estensione del menu di scelta rapida è un server COM in-process che implementa determinate interfacce ed è registrato con Active Directory Domain Services.

**Per creare e installare un'estensione del menu di scelta rapida**

1.  Creare la DLL dell'estensione del menu di scelta rapida. Un'estensione del menu di scelta rapida è un server COM in-process che, come minimo, implementa le [**interfacce IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) Per altre informazioni, vedere [Implementazione dell'oggetto COM del menu di scelta rapida.](implementing-the-context-menu-com-object.md)
2.  Installare l'estensione del foglio del menu di scelta rapida nei computer in cui viene usata l'estensione del menu di scelta rapida. Questa operazione viene eseguita creando un pacchetto di Microsoft Windows Installer per la DLL dell'estensione del menu di scelta rapida e distribuendo il pacchetto in modo appropriato usando i criteri di gruppo. Per altre informazioni, vedere [Distribuzione di Interfaccia utente componenti](distributing-user-interface-components.md).
3.  Registrare l'estensione del menu di scelta rapida nel registro Windows e con Active Directory Domain Services. Per altre informazioni, vedere [Registrazione dell'oggetto COM del menu](registering-the-context-menu-com-object-in-a-display-specifier.md)di scelta rapida in un identificatore di visualizzazione.

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a>Estensione del menu di scelta rapida con una voce di menu di scelta rapida statica

Una voce di menu di scelta rapida statica può essere usata per richiamare qualsiasi file avviato con l'API [**ShellExecute,**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) ad esempio un URL di applicazione o di pagina Web. A tale scopo, è necessario registrare la voce di menu di scelta rapida statica per una determinata classe di oggetti in modo che la voce di menu di scelta rapida statica sia aggiunta al menu di scelta rapida degli oggetti di tale classe. Per altre informazioni, vedere [Registrazione di una voce di menu di scelta rapida statica.](registering-a-static-context-menu-item.md)

 

 