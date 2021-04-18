---
title: Implementazione dell'oggetto COM del menu di scelta rapida
description: Un'estensione del menu di scelta rapida è un oggetto COM implementato come server in-process.
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- oggetto COM del menu di scelta rapida
- oggetto COM del menu di scelta rapida, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34d6b487d130327b379ed845f2d0157f2b28056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299569"
---
# <a name="implementing-the-context-menu-com-object"></a>Implementazione dell'oggetto COM del menu di scelta rapida

Un'estensione del menu di scelta rapida è un oggetto COM implementato come server in-process. L'estensione del menu di scelta rapida deve implementare le interfacce [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Viene creata un'istanza dell'estensione del menu di scelta rapida quando l'utente Visualizza il menu di scelta rapida per un oggetto di una classe per la quale è stata registrata l'estensione del menu di scelta rapida.

## <a name="implementing-ishellextinit"></a>Implementazione di IShellExtInit

Quando viene creata un'istanza dell'oggetto COM dell'estensione del menu di scelta rapida, viene chiamato il metodo [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . **IShellExtInit:: Initialize** fornisce l'estensione del menu di scelta rapida con un oggetto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) che contiene i dati pertinenti all'oggetto directory a cui si applica il menu di scelta rapida.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene i dati nel formato [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . Il formato dati **CFSTR \_ DSOBJECTNAMES** è un **HGLOBAL** che contiene una struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . La struttura **DSOBJECTNAMES** contiene i dati relativi all'oggetto directory a cui viene applicata l'estensione della finestra delle proprietà.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene inoltre dati nel formato delle [**Opzioni di \_ visualizzazione delle \_ \_ specifiche \_ di CFSTR DS**](cfstr-ds-display-spec-options.md) . Il formato dei dati delle **\_ \_ \_ \_ Opzioni di visualizzazione di CFSTR DS** è un **HGLOBAL** che contiene una struttura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . **DSDISPLAYSPECOPTIONS** contiene i dati di configurazione per l'utilizzo da parte dell'estensione.

Se un valore diverso da **S \_ OK** viene restituito da [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), l'estensione del menu di scelta rapida non verrà utilizzata.

I parametri *pidlFolder* e *HkeyProgID* del metodo [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) non vengono usati.

## <a name="implementing-icontextmenu"></a>Implementazione di IContextMenu

Dopo che [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) restituisce, viene chiamato il metodo [**IContextMenu:: QueryContextMenu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) per ottenere la voce di menu o gli elementi che verrà aggiunta dall'estensione del menu di scelta rapida. L'implementazione di **QueryContextMenu** è piuttosto semplice. L'estensione del menu di scelta rapida aggiunge le voci di menu utilizzando [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) o una funzione simile. Gli identificatori dei comandi di menu devono essere maggiori o uguali a *idCmdFirst* e devono essere minori di *idCmdLast*. **QueryContextMenu** deve restituire l'identificatore numerico più grande aggiunto al menu più uno. Il modo migliore per assegnare gli identificatori dei comandi di menu è iniziare da zero e lavorare in sequenza. Se l'estensione del menu di scelta rapida non richiede alcuna voce di menu, non deve semplicemente aggiungere elementi al menu e restituire zero da **QueryContextMenu**.

[**IContextMenu:: GetCommandString**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) viene chiamato per recuperare i dati testuali per la voce di menu, ad esempio il testo della guida da visualizzare per la voce di menu. È possibile che l'host del menu di scelta rapida usi stringhe Unicode mentre l'estensione usa stringhe ANSI. Per questo motivo, i case **cataloghi globali \_ HELPTEXTA**, **cataloghi globali \_ HELPTEXTW**, cataloghi **globali \_ Verba** e **cataloghi globali \_ VERBW** devono essere gestiti singolarmente. L'implementazione di questo metodo è facoltativa.

[**IContextMenu:: InvokeCommand**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) viene chiamato quando viene selezionata una delle voci di menu installate dall'estensione del menu di scelta rapida. Il menu di scelta rapida consente di eseguire o avviare le azioni desiderate in risposta a questo metodo.

 

 