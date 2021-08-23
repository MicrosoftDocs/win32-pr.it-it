---
title: Codici di errore Win32 per ADSI
description: I codici di errore Win32 standard vengono usati anche per restituire messaggi di errore ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Codici di errore Win32 per ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b18539e93504991f244bbba8b41b13e524ff236918145deda73788169cef368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589741"
---
# <a name="win32-error-codes-for-adsi"></a>Codici di errore Win32 per ADSI

I codici di errore Win32 standard vengono usati anche per restituire messaggi di errore ADSI. In particolare, il provider LDAP ADSI esegue il mapping di tutti i codici di errore LDAP ai codici di errore Win32. I valori **HRESULT** di questi codici di errore sono nel formato 0x8007XXXX, dove le ultime quattro cifre esadecimali, XXXX, corrispondono ai valori **DWORD** del codice di errore Win32 appropriato. Ad esempio, il valore di errore ADSI 0x80072020 il valore di errore Win32 0x2020 in formato esadecimale o 8224 in decimale.

Per convertire il valore **HRESULT** di un codice di errore ADSI, restituito dall'applicazione, nel valore **DWORD** dell'errore Win32 corrispondente, come definito nei file di intestazione precedenti, usare la procedura seguente.

La maggior parte dei codici di errore Win32 per ADSI è definita in Winerror.h o Lmerr.h. I valori di errore sono elencati come valori decimali in questi file.

**Per convertire il **valore HRESULT** di un codice di errore ADSI nel valore **DWORD** dell'errore Win32 corrispondente**

1.  Convertire il **valore HRESULT** in un numero esadecimale se si inizia con un valore decimale, come si può ottenere da un'Visual Basic applicazione.
2.  Eliminare il 0x8007 parte che produce il resto.
3.  Convertire il resto in un numero decimale.
4.  Cercare il resto decimale in Winerror.h.
5.  Se non viene trovato in Winerror.h, sottrarre 2100 dal resto decimale e cercare il risultato in Lmerr.h.

ADSI 2.0 esegue il mapping dei codici di errore LDAP a un set di codici di errore Win32 diverso da quello usato in ADSI per Windows 2000 e DS Client. Le differenze sono elencate in:

-   [Codici di errore Win32](win32-error-codes.md)
-   [Codici di errore Win32 per ADSI 2.0](win32-error-codes-for-adsi-2-0.md)

 

 




