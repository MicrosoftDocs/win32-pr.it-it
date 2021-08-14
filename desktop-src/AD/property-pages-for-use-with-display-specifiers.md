---
title: Pagine delle proprietà da usare con identificatori di visualizzazione
description: Active Directory Domain Services un meccanismo per l'aggiunta di pagine alla finestra delle proprietà visualizzata per un oggetto directory dagli snap-in amministrativi di Active Directory o dalla shell Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- identificatori di visualizzazione AD, pagine delle proprietà da usare con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f813223aa88dce3b8bba867139bab476416cba1932c583e2e9be591de03fc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185185"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>Pagine delle proprietà da usare con identificatori di visualizzazione

Active Directory Domain Services un meccanismo per l'aggiunta di pagine alla finestra delle proprietà visualizzata per un oggetto directory dagli snap-in amministrativi di Active Directory o dalla shell Windows. Per aggiungere una pagina alla finestra delle proprietà, implementare un'estensione della finestra delle proprietà.

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione presuppone che il lettore abbia familiarità con le operazioni COM e lo sviluppo di componenti con C++. Attualmente non è possibile creare un'estensione della finestra delle proprietà di Active Directory usando Visual Basic.

## <a name="creating-an-active-directory-property-sheet-extension"></a>Creazione di un'estensione della finestra delle proprietà di Active Directory

*Un'estensione della finestra delle* proprietà è un server COM in-process che implementa determinate interfacce e viene registrato con Active Directory Domain Services. Per creare un'estensione della finestra delle proprietà, seguire questa procedura.

**Per creare un'estensione della finestra delle proprietà di Active Directory**

1.  Creare la DLL di estensione della finestra delle proprietà. Un'estensione della finestra delle proprietà è un server COM in-process che, come minimo, implementa le interfacce [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) Per altre informazioni, vedere [Implementazione dell'oggetto COM della pagina delle proprietà](implementing-the-property-page-com-object.md).
2.  Installare l'estensione della finestra delle proprietà nei computer in cui deve essere usata l'estensione della finestra delle proprietà. A tale scopo, creare un pacchetto microsoft Windows Installer per la DLL dell'estensione della finestra delle proprietà e distribuire il pacchetto in modo appropriato usando i criteri di gruppo. Per altre informazioni, vedere [Distribuzione di Interfaccia utente componenti](distributing-user-interface-components.md).
3.  Registrare l'estensione della finestra delle proprietà nel registro Windows e con Active Directory Domain Services. Per altre informazioni, vedere [Registrazione dell'oggetto COM della pagina](registering-the-property-page-com-object-in-a-display-specifier.md)delle proprietà in un identificatore di visualizzazione .

 

 