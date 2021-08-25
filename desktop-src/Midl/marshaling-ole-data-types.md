---
title: Marshalling dei tipi di dati OLE
description: Marshalling di automazione e tipi di dati OLE.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL e COM MIDL , marshalling dei tipi di dati OLE
- marshalling MIDL
- MIDL dei dati OLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91c5f1527ffaa361b85550941af1538c99251e59750b27f3bfe7552251e821e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895021"
---
# <a name="marshaling-ole-data-types"></a>Marshalling dei tipi di dati OLE

Per semplificare l'uso di determinati tipi di dati OLE e di automazione, nonché di alcuni handle di sistema usati di frequente in COM, i typedef per questi tipi di dati e le relative funzioni helper correlate sono disponibili importando file IDL di Windows e collegandoli ai file DLL OLE e Automation. Questi file vengono installati automaticamente nel sistema.

-   Per usare il tipo di dati [**BSTR**](/previous-versions/windows/desktop/automat/bstr) nelle chiamate di procedura remota, importare il file wtypes.idl nel file di definizione dell'interfaccia (IDL) e collegarsi a Oleaut32.lib durante la compilazione dell'applicazione distribuita. In questo modo, gli stub useranno le funzioni helper già pronte **BSTR \_ UserSize**, **BSTR \_ UserMarshal**, **BSTR \_ UserUnmarshal** e **BSTR \_ UserFree**.
-   Per usare altri tipi di dati di Automazione, ad esempio [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) e [**SAFEARRAY,**](/windows/win32/api/oaidl/ns-oaidl-safearray)o tipi che usano tali tipi (ad [**esempio, DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) ed [**EXCEPINFO),**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)importare il file objidl.idl nel file IDL e collegarsi a oleaut32.lib in fase di compilazione. In questo modo sarà possibile usare le routine helper appropriate.
-   Per usare tipi di dati OLE (ad esempio CLIPFORMAT, SNB, STGMEDIUM, ASYNC STGMEDIUM) o handle di sistema (ad esempio \_ HMETAFILE \_ PICT, HENHMETAFILE, HMETAFILE, HBITMAP, HPALETTE e HGLOBAL), importare il file objidl.idl nel file di definizione dell'interfaccia e collegarsi a ole32.lib in fase di compilazione.
-   Anche gli handle OLE seguenti vengono definiti con l'attributo **\[ \_ wire marshal, \]** ma solo come handle all'interno di un computer perché non possono essere usati in chiamate di procedura remota ad altri computer in questo momento: HWND, HMENU, HACCEL, HDC, HFONT, HICON, HBRUSH. Importare il file objidl.idl nel file IDL e collegarsi a ole32.lib in fase di compilazione per usare questi handle nella comunicazione interprocesso in un singolo computer.

Per altre informazioni, vedere Attributo wire [ \_ marshal](/windows/desktop/Rpc/the-wire-marshal-attribute), Il tipo [ \_ UserSize Function](/windows/desktop/Rpc/the-type-usersize-function), Il tipo [ \_ UserMarshal Function](/windows/desktop/Rpc/the-type-usermarshal-function), Il tipo [ \_ UserUnmarshal Function](/windows/desktop/Rpc/the-type-userunmarshal-function), The type [ \_ UserFree Function](/windows/desktop/Rpc/the-type-userfree-function)e [Targeting Stubs for Specific 32-bit or 64-bit Platforms](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md).

 

 