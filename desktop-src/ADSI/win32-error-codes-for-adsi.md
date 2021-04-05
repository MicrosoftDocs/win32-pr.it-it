---
title: Codici di errore Win32 per ADSI
description: I codici di errore Win32 standard vengono inoltre utilizzati per restituire messaggi di errore ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Codici di errore Win32 per ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707348"
---
# <a name="win32-error-codes-for-adsi"></a>Codici di errore Win32 per ADSI

I codici di errore Win32 standard vengono inoltre utilizzati per restituire messaggi di errore ADSI. In particolare, il provider LDAP ADSI esegue il mapping di tutti i codici di errore LDAP ai codici di errore Win32. I valori **HRESULT** di questi codici di errore sono del formato 0x8007XXXX, dove le ultime quattro cifre esadecimali, xxxx, corrispondono ai valori **DWORD** del codice di errore Win32 appropriato. Il valore di errore ADSI 0x80072020, ad esempio, restituisce il valore di errore Win32 di 0x2020 in formato esadecimale o 8224 in decimale.

Per convertire il valore **HRESULT** di un codice di errore ADSI, restituito dall'applicazione, nel valore **DWORD** dell'errore Win32 corrispondente, come definito nei file di intestazione precedenti, utilizzare la procedura seguente.

La maggior parte dei codici di errore Win32 per ADSI è definita in Winerror. h o Lmerr. h. I valori di errore sono elencati come valori decimali in questi file.

**Per convertire il valore **HRESULT** di un codice di errore ADSI nel valore **DWORD** dell'errore Win32 corrispondente**

1.  Convertire il valore **HRESULT** in un numero esadecimale se si inizia con un valore decimale, come si può ottenere da un'applicazione Visual Basic.
2.  Rilasciare la parte 0x8007 per produrre il resto.
3.  Converte il resto in un numero decimale.
4.  Cercare il resto decimale in Winerror. h.
5.  Se non viene trovato in Winerror. h, sottrarre 2100 dal resto decimale e cercare il risultato in Lmerr. h.

ADSI 2,0 esegue il mapping dei codici di errore LDAP a un set di codici di errore Win32 diverso da quello usato in ADSI per Windows 2000 e il client DS. Le differenze sono elencate in:

-   [Codici di errore Win32](win32-error-codes.md)
-   [Codici di errore Win32 per ADSI 2,0](win32-error-codes-for-adsi-2-0.md)

 

 




