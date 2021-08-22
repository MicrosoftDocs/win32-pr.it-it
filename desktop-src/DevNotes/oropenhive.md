---
description: Carica il file hive del Registro di sistema specificato in memoria e convalida l'hive.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Funzione OROpenHive (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 86ff3d6ff15b030054d40ca7131e521cedb59ebf20c4942951f0e141f27a2840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076015"
---
# <a name="oropenhive-function"></a>Funzione OROpenHive

Carica il file hive del Registro di sistema specificato in memoria e convalida l'hive.

## <a name="syntax"></a>Sintassi


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpHivePath* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode che specifica il nome del file hive del Registro di sistema da caricare in memoria. Può trattarsi di un file hive salvato con la funzione [**ORSaveHive**](orsavehive.md) o creato con la funzione [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx.](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) Le dimensioni del file devono essere inferiori a 4 GB e il chiamante deve disporre dell'accesso FILE \_ READ \_ DATA al file. Per altre informazioni, vedere [Sicurezza dei file e diritti di accesso.](../fileio/file-security-and-access-rights.md)

</dd> <dt>

*phkResult* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un handle per la chiave radice dell'hive del Registro di sistema offline caricato. Se non è possibile aprire il file hive del Registro di sistema o la convalida non riesce, la funzione imposta questo parametro su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore. I codici di errore possibili sono i seguenti:

-   Se il file è vuoto o di dimensioni maggiori di 4 GB, la funzione restituisce ERROR \_ BADDB.
-   Se il chiamante non dispone dei diritti di accesso necessari per aprire il file, la funzione restituisce ERROR \_ ACCESS \_ DENIED.
-   Se la convalida dell'hive del Registro di sistema non riesce, la funzione restituisce ERROR \_ NOT \_ REGISTRY \_ FILE.

## <a name="remarks"></a>Commenti

La **funzione OROpenHive** è l'unica funzione del Registro di sistema offline che convalida un hive del Registro di sistema. Se la convalida non riesce, non viene effettuato alcun tentativo di ripristinare l'hive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria del Registro di sistema offline versione 1.0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[Regsavekey](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
