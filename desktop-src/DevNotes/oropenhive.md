---
description: Carica il file hive del registro di sistema specificato in memoria e convalida l'hive.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Funzione OROpenHive (offreg. h)
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
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330862"
---
# <a name="oropenhive-function"></a>OROpenHive (funzione)

Carica il file hive del registro di sistema specificato in memoria e convalida l'hive.

## <a name="syntax"></a>Sintassi


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpHivePath* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode che specifica il nome del file hive del registro di sistema da caricare in memoria. Può trattarsi di un file hive salvato con la funzione [**ORSaveHive**](orsavehive.md) o creato con la funzione [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) . Il file deve avere una dimensione inferiore a 4 GB e il chiamante deve avere accesso ai \_ \_ dati di lettura del file. Per ulteriori informazioni, vedere [sicurezza dei file e diritti di accesso](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un handle per la chiave radice dell'hive del registro di sistema offline caricato. Se non è possibile aprire il file hive del registro di sistema o la convalida ha esito negativo, la funzione imposta questo parametro su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag. I codici di errore possibili includono i seguenti:

-   Se la dimensione del file è vuota o maggiore di 4 GB, la funzione restituisce l'errore \_ BADDB.
-   Se il chiamante non dispone dei diritti di accesso necessari per aprire il file, la funzione restituisce l'errore di \_ accesso \_ negato.
-   Se la convalida dell'hive del registro di sistema non riesce, la funzione restituisce un errore \_ non il \_ file del registro \_

## <a name="remarks"></a>Commenti

La funzione **OROpenHive** è l'unica funzione del registro di sistema offline che convalida un hive del registro di sistema. Se la convalida ha esito negativo, non viene effettuato alcun tentativo di ripristinare l'hive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
