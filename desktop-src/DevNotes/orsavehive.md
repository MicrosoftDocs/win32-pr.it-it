---
description: Scrive l'hive del registro di sistema offline specificato in un file.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Funzione ORSaveHive (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325102"
---
# <a name="orsavehive-function"></a>ORSaveHive (funzione)

Scrive l'hive del registro di sistema offline specificato in un file.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Handle per l'hive del registro di sistema offline da salvare.

</dd> <dt>

*lpHivePath* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode che specifica il nome del file hive del registro di sistema. Non può corrispondere al nome di un file esistente.

</dd> <dt>

*dwOsMajorVersion* \[ in\]
</dt> <dd>

Numero di versione principale del sistema operativo. Il membro può essere uno dei valori seguenti.



| Valore                                                                        | Significato                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>5</dt> </dl> | Se *dwOsMinorVersion* è 1, il sistema operativo è Windows XP.<br/> Se *dwOsMinorVersion* è 2, il sistema operativo è windows Server 2003 R2, windows Server 2003 o Windows XP Professional x64 Edition.<br/> |
| <dl> <dt>6</dt> </dl> | Se *dwOsMinorVersion* è 0, il sistema operativo è windows Server 2008 o Windows Vista.<br/> Se *dwOsMinorVersion* è 1, il sistema operativo è windows Server 2008 R2 o Windows 7.<br/>                       |



 

</dd> <dt>

*dwOsMinorVersion* \[ in\]
</dt> <dd>

Numero di versione secondario del sistema operativo. Il membro può essere uno dei valori seguenti.



| Valore                                                                        | Significato                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Se *dwOsMajorVersion* è 6, il sistema operativo è windows Server 2008 o Windows Vista.<br/>                                                                                                                                          |
| <dl> <dt>1</dt> </dl> | Se *dwOsMajorVersion* è 5, il sistema operativo è Windows XP.<br/> Se *dwOsMajorVersion* è 6, il sistema operativo è windows Server 2008 R2 o Windows 7.<br/>                                                                |
| <dl> <dt>2</dt> </dl> | Se *dwOsMajorVersion* è 5, il sistema operativo è windows Server 2003 R2, windows Server 2003 o Windows XP Professional x64 Edition. <br/> Se *dwOsMajorVersion* è 6, il parametro *dwOsMinorVersion* deve essere 0 o 1. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag. I codici di errore possibili includono i seguenti:

-   Se il chiamante non dispone dei diritti di accesso necessari per scrivere il file, la funzione restituisce l'errore di \_ accesso \_ negato.
-   Se il file specificato esiste già, la funzione restituisce un errore \_ già \_ esistente.

## <a name="remarks"></a>Commenti

Per salvare le modifiche apportate a un hive del registro di sistema offline, è necessario usare la funzione **ORSaveHive** . Le modifiche non vengono mantenute fino a quando non viene chiamato **ORSaveHive** per salvare l'hive in un file.

I parametri *dwOsMajorVersion* e *dwOsMinorVersion* insieme specificano il formato di destinazione del file hive del registro di sistema. Nella tabella seguente sono riepilogati i numeri di versione del sistema operativo più recenti.



| Sistema operativo                    | Numero di versione |
|-------------------------------------|----------------|
| Windows Server 2008 R2              | 6.1            |
| Windows 7                           | 6.1            |
| Windows Server 2008                 | 6.0            |
| Windows Vista                       | 6.0            |
| Windows Server 2003 R2              | 5,2            |
| Windows Server 2003                 | 5,2            |
| Windows XP Professional x64 Edition | 5,2            |
| Windows XP                          | 5.1            |



 

Utilizzare la funzione [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) per recuperare le informazioni sul sistema operativo corrente.

La funzione **ORSaveHive** blocca l'hive del registro di sistema mentre scrive l'hive nel file, quindi chiude il file e rilascia il blocco. L'hive del registro di sistema rimane in memoria fino a quando non viene chiuso chiamando la funzione [**ORCloseHive**](orclosehive.md) . È possibile apportare ulteriori modifiche all'hive del registro di sistema mentre è aperto. Tuttavia, per mantenere queste modifiche, è necessario salvare l'hive in un nuovo file, perché la funzione **ORSaveHive** non sovrascriverà un file esistente.

La funzione **ORSaveHive** può essere usata per salvare parte dell'hive del registro di sistema offline. La chiave specificata nel parametro *handle* diventa la chiave radice di un hive costituita dalla chiave specificata e da tutte le relative sottochiavi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
