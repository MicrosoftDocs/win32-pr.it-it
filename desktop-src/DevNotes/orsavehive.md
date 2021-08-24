---
description: Scrive l'hive del Registro di sistema offline specificato in un file.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Funzione ORSaveHive (Offreg.h)
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
ms.openlocfilehash: 0b4dde44b6cc6d2c5cfd80f4041cd6370f680eb6ca867e9e8f2bbce5f0702e27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758511"
---
# <a name="orsavehive-function"></a>ORSaveHive - funzione

Scrive l'hive del Registro di sistema offline specificato in un file.

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

*Handle* \[ Pollici\]
</dt> <dd>

Handle per l'hive del Registro di sistema offline da salvare.

</dd> <dt>

*lpHivePath* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode che specifica il nome del file hive del Registro di sistema. Non può essere il nome di un file esistente.

</dd> <dt>

*dwOsMajorVersion* \[ Pollici\]
</dt> <dd>

Numero di versione principale del sistema operativo. Questo membro può essere uno dei valori seguenti.



| Valore                                                                        | Significato                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>5</dt> </dl> | Se *dwOsMinorVersion* è 1, il sistema operativo è Windows XP.<br/> Se *dwOsMinorVersion* è 2, il sistema operativo è Windows Server 2003 R2, Windows Server 2003 o Windows XP Professional x64 Edition.<br/> |
| <dl> <dt>6</dt> </dl> | Se *dwOsMinorVersion* è 0, il sistema operativo è Windows Server 2008 o Windows Vista.<br/> Se *dwOsMinorVersion* è 1, il sistema operativo è Windows Server 2008 R2 o Windows 7.<br/>                       |



 

</dd> <dt>

*dwOsMinorVersion* \[ Pollici\]
</dt> <dd>

Numero di versione secondaria del sistema operativo. Questo membro può essere uno dei valori seguenti.



| Valore                                                                        | Significato                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Se *dwOsMajorVersion* è 6, il sistema operativo Windows Server 2008 o Windows Vista.<br/>                                                                                                                                          |
| <dl> <dt>1</dt> </dl> | Se *dwOsMajorVersion* è 5, il sistema operativo è Windows XP.<br/> Se *dwOsMajorVersion* è 6, il sistema operativo è Windows Server 2008 R2 o Windows 7.<br/>                                                                |
| <dl> <dt>2</dt> </dl> | Se *dwOsMajorVersion* è 5, il sistema operativo è Windows Server 2003 R2, Windows Server 2003 o Windows XP Professional x64 Edition. <br/> Se *dwOsMajorVersion* è 6, il *parametro dwOsMinorVersion* deve essere 0 o 1. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore. I codici di errore possibili sono i seguenti:

-   Se il chiamante non dispone dei diritti di accesso necessari per scrivere il file, la funzione restituisce ERROR \_ ACCESS \_ DENIED.
-   Se il file specificato esiste già, la funzione restituisce ERROR \_ ALREADY \_ EXISTS.

## <a name="remarks"></a>Commenti

La **funzione ORSaveHive** deve essere usata per salvare le modifiche apportate a un hive del Registro di sistema offline. Le modifiche non vengono mantenute fino **a quando non viene chiamato ORSaveHive** per salvare l'hive in un file.

I *parametri dwOsMajorVersion* e *dwOsMinorVersion* insieme specificano il formato di destinazione del file hive del Registro di sistema. Nella tabella seguente sono riepilogati i numeri di versione del sistema operativo più recenti.



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



 

Usare la [funzione GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) per recuperare informazioni sul sistema operativo corrente.

La **funzione ORSaveHive** blocca l'hive del Registro di sistema durante la scrittura dell'hive nel file, quindi chiude il file e rilascia il blocco. L'hive del Registro di sistema rimane in memoria fino a quando non viene chiuso chiamando la [**funzione ORCloseHive.**](orclosehive.md) È possibile apportare ulteriori modifiche all'hive del Registro di sistema mentre è aperto. Tuttavia, per mantenere queste modifiche, l'hive deve essere salvato in un nuovo file, perché la funzione **ORSaveHive** non sovrascriverà un file esistente.

La **funzione ORSaveHive** può essere usata per salvare parte dell'hive del Registro di sistema offline. La chiave specificata nel *parametro Handle* diventa la chiave radice di un hive costituito dalla chiave specificata e da tutte le relative sottochiavi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria del Registro di sistema offline versione 1.0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Getversionex](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
