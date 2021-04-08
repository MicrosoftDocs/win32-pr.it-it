---
title: Pagine delle proprietà da usare con gli identificatori di visualizzazione
description: Active Directory Domain Services fornire un meccanismo per aggiungere pagine alla finestra delle proprietà visualizzata per un oggetto directory da Active Directory snap-in amministrativi o dalla shell di Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- Visualizza gli identificatori AD, le pagine delle proprietà da usare con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872274"
---
# <a name="property-pages-for-use-with-display-specifiers"></a>Pagine delle proprietà da usare con gli identificatori di visualizzazione

Active Directory Domain Services fornire un meccanismo per aggiungere pagine alla finestra delle proprietà visualizzata per un oggetto directory da Active Directory snap-in amministrativi o dalla shell di Windows. Per aggiungere una pagina alla finestra delle proprietà, implementare un'estensione della finestra delle proprietà.

## <a name="developer-audience"></a>Sviluppatori

In questa documentazione si presuppone che il lettore abbia familiarità con l'operazione COM e lo sviluppo di componenti con C++. Non è attualmente possibile creare un'estensione della finestra delle proprietà Active Directory utilizzando Visual Basic.

## <a name="creating-an-active-directory-property-sheet-extension"></a>Creazione di un'estensione della finestra delle proprietà Active Directory

Un' *estensione della finestra delle proprietà* è un server com in-process che implementa determinate interfacce e viene registrato con Active Directory Domain Services. Per creare un'estensione della finestra delle proprietà, seguire questa procedura.

**Per creare un'estensione della finestra delle proprietà Active Directory**

1.  Creare la DLL di estensione della finestra delle proprietà. Un'estensione della finestra delle proprietà è un server COM in-process che implementa come minimo le interfacce [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Per ulteriori informazioni, vedere [implementazione dell'oggetto com della pagina delle proprietà](implementing-the-property-page-com-object.md).
2.  Installare l'estensione della finestra delle proprietà nei computer in cui deve essere utilizzata l'estensione della finestra delle proprietà. A tale scopo, creare un pacchetto di Microsoft Windows Installer per la DLL di estensione della finestra delle proprietà e distribuire il pacchetto in modo appropriato utilizzando i criteri di gruppo. Per ulteriori informazioni, vedere la pagina relativa alla [distribuzione dei componenti dell'interfaccia utente](distributing-user-interface-components.md).
3.  Registrare l'estensione della finestra delle proprietà nel registro di sistema di Windows e con Active Directory Domain Services. Per ulteriori informazioni, vedere [la pagina relativa alla registrazione dell'oggetto com della pagina delle proprietà in un identificatore di visualizzazione](registering-the-property-page-com-object-in-a-display-specifier.md).

 

 