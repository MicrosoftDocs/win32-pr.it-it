---
title: Implementazione dell'oggetto COM del menu di scelta rapida
description: Un'estensione del menu di scelta rapida è un oggetto COM implementato come server in-process.
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- oggetto COM del menu di scelta rapida AD
- oggetto COM del menu di scelta rapida AD, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac371ea64239c18de2a8f30c969eb6d920221f0a802f18ceeebfef2c3991e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187649"
---
# <a name="implementing-the-context-menu-com-object"></a>Implementazione dell'oggetto COM del menu di scelta rapida

Un'estensione del menu di scelta rapida è un oggetto COM implementato come server in-process. L'estensione del menu di scelta rapida deve implementare le interfacce [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) [**e IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) Viene creata un'istanza di un'estensione del menu di scelta rapida quando l'utente visualizza il menu di scelta rapida per un oggetto di una classe per cui è stata registrata l'estensione del menu di scelta rapida.

## <a name="implementing-ishellextinit"></a>Implementazione di IShellExtInit

Dopo aver creato un'istanza dell'oggetto COM dell'estensione del menu di scelta rapida, viene chiamato il metodo [**IShellExtInit::Initialize.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) **IShellExtInit::Initialize** fornisce l'estensione del menu di scelta rapida con un oggetto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) che contiene i dati pertinenti all'oggetto directory a cui si applica il menu di scelta rapida.

[**L'oggetto IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene dati nel [**formato \_ CFSTR DSOBJECTNAMES.**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) Il **formato dati \_ CFSTR DSOBJECTNAMES** è **un HGLOBAL** che contiene una [**struttura DSOBJECTNAMES.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) La **struttura DSOBJECTNAMES contiene i** dati sull'oggetto directory a cui si applica l'estensione della finestra delle proprietà.

[**L'oggetto IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene anche dati nel formato [**CFSTR \_ DS \_ DISPLAY SPEC \_ \_ OPTIONS.**](cfstr-ds-display-spec-options.md) Il **formato dati CFSTR \_ DS DISPLAY SPEC \_ \_ \_ OPTIONS** è un **formato HGLOBAL** che contiene una struttura [**DSDISPLAYSPECOPTIONS.**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) **DSDISPLAYSPECOPTIONS contiene i** dati di configurazione per l'uso da parte dell'estensione.

Se un valore diverso da **S \_ OK** viene restituito da [**IShellExtInit::Initialize,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)l'estensione del menu di scelta rapida non verrà usata.

I *parametri pidlFolder* *e hkeyProgID* del metodo [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) non vengono usati.

## <a name="implementing-icontextmenu"></a>Implementazione di IContextMenu

Dopo il ritorno [**di IShellExtInit::Initialize,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) viene chiamato il metodo [**IContextMenu::QueryContextMenu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) per ottenere la voce di menu o le voci che verranno aggiunti dall'estensione del menu di scelta rapida. **L'implementazione di QueryContextMenu** è piuttosto semplice. L'estensione del menu di scelta rapida aggiunge le voci di menu usando [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) o una funzione simile. Gli identificatori dei comandi di menu devono essere maggiori o uguali a *idCmdFirst* e devono essere minori di *idCmdLast.* **QueryContextMenu** deve restituire l'identificatore numerico più grande aggiunto al menu più uno. Il modo migliore per assegnare gli identificatori dei comandi di menu è iniziare da zero e lavorare in sequenza. Se l'estensione del menu di scelta rapida non richiede alcuna voce di menu, non deve semplicemente aggiungere voci al menu e restituire zero da **QueryContextMenu.**

[**IContextMenu::GetCommandString**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) viene chiamato per recuperare i dati testuali per la voce di menu, ad esempio il testo della Guida da visualizzare per la voce di menu. È possibile che l'host del menu di scelta rapida usi stringhe Unicode mentre l'estensione usa stringhe ANSI. Per questo problema, i case **GCS \_ HELPTEXTA**, **GCS \_ HELPTEXTW**, **GCS \_ VERBA** e **GCS \_ VERBW** devono essere gestiti singolarmente. L'implementazione di questo metodo è facoltativa.

[**IContextMenu::InvokeCommand**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) viene chiamato quando viene selezionata una delle voci di menu installate dall'estensione del menu di scelta rapida. Il menu di scelta rapida esegue o avvia le azioni desiderate in risposta a questo metodo.

 

 