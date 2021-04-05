---
title: Marshalling di tipi di dati OLE
description: Marshalling di automazione e tipi di dati OLE.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL e COM MIDL, marshalling di tipi di dati OLE
- marshalling MIDL
- MIDL di dati OLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970c6e0fef9d0fc88b8a0a11a087fa4396d7a7c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725154"
---
# <a name="marshaling-ole-data-types"></a>Marshalling di tipi di dati OLE

Per semplificare l'utilizzo di determinati tipi di dati di automazione e OLE, oltre ad alcuni handle di sistema usati di frequente in COM, i typedef per questi tipi di dati e le funzioni di supporto correlate sono disponibili mediante l'importazione dei file IDL di Windows e il collegamento ai file DLL OLE e di automazione. Questi file vengono installati automaticamente nel sistema.

-   Per utilizzare il tipo di dati [**BSTR**](/previous-versions/windows/desktop/automat/bstr) in Remote Procedure Calls, importare il file wtypes. idl nel file di definizione dell'interfaccia (IDL) e collegarsi a Oleaut32. lib durante la compilazione dell'applicazione distribuita. In questo consentirà agli stub di usare le funzioni di supporto **predefinite \_ BSTR UserSize**, **BSTR \_ UserMarshal**, **BSTR \_ UserUnmarshal** e **BSTR \_ UserFree**.
-   Per utilizzare altri tipi di dati di automazione, come [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) e [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray), o tipi che utilizzano tali tipi (ad esempio, [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) e [**EXCEPINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)), importare il file objidl. idl nel file IDL e collegarsi a Oleaut32. lib in fase di compilazione. Questo consentirà di usare le routine di supporto appropriate.
-   Per usare i tipi di dati OLE (ad esempio CLIPFORMAT, BNS, STGMEDIUM, ASYNC \_ STGMEDIUM) o gli handle di sistema (ad esempio HMETAFILE \_ PICT, HENHMETAFILE, HMETAFILE, HBITMAP, HPALETTE e HGLOBAL), importare il file objidl. idl nel file di definizione dell'interfaccia e collegarsi a ole32. lib in fase di compilazione.
-   Gli handle OLE seguenti sono definiti anche con l'attributo **\[ Wire \_ marshalling \]** , ma solo come handle all'interno di un computer, in quanto non possono essere usati nelle chiamate di procedura remota ad altri computer al momento: HWND, HMENU, haccel, HDC, HFONT, HICON, HBRUSH. Importare il file objidl. idl nel file IDL e collegarsi a ole32. lib in fase di compilazione per usare questi handle nella comunicazione interprocesso in un singolo computer.

Per ulteriori informazioni, vedere [l' \_ attributo Wire Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute), [il tipo \_ UserSize Function](/windows/desktop/Rpc/the-type-usersize-function), [il tipo \_ UserMarshal Function](/windows/desktop/Rpc/the-type-usermarshal-function), [il tipo \_ UserUnmarshal Function](/windows/desktop/Rpc/the-type-userunmarshal-function), [il tipo \_ UserFree function](/windows/desktop/Rpc/the-type-userfree-function)e gli [Stub targeting per specifiche piattaforme a 32 bit o a 64 bit](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md).

 

 