---
title: Funzione di callback RasAdminReleaseIpAddress
description: La funzione RasAdminReleaseIpAddress è una funzione definita dall'applicazione esportata da una DLL di amministrazione del server RAS di terze parti.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- Funzione di callback RasAdminReleaseIpAddress RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 102c9af7a8e38ccbbb4a7e67b2734588857ddca93da862be211fd1223133f80d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788863"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>Funzione di callback RasAdminReleaseIpAddress

\[La **funzione RasAdminReleaseIpAddress** è disponibile per l'uso in Windows NT 4.0 e non è disponibile nelle versioni successive. Usare invece [**MprAdminReleaseIpAddress.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)\]

La **funzione RasAdminReleaseIpAddress** è una funzione definita dall'applicazione esportata da una DLL di amministrazione del server RAS di terze parti. RAS chiama questa funzione per notificare alla DLL che il client remoto è stato disconnesso e che l'indirizzo IP deve essere rilasciato.

## <a name="syntax"></a>Sintassi


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszUserName* \[ Pollici\]
</dt> <dd>

Specifica il puntatore a una stringa Unicode con terminazione Null che specifica il nome di un utente remoto per il quale in precedenza è stato ottenuto un indirizzo IP usando la [**funzione RasAdminGetIpAddressForUser.**](rasadmingetipaddressforuser.md)

</dd> <dt>

*lpszPortName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome della porta su cui è connesso l'utente specificato da *lpszUserName.*

</dd> <dt>

*pipAddress* \[ Pollici\]
</dt> <dd>

Puntatore a **una variabile IPADDR** che specifica l'indirizzo IP restituito per questo utente in una chiamata precedente a [**RasAdminGetIpAddressForUser.**](rasadmingetipaddressforuser.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non sono disponibili informazioni estese sugli errori per questa funzione. non chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Il server RAS chiama la **funzione RasAdminReleaseIpAddress** solo se l'applicazione ha restituito **TRUE** nel parametro *bNotifyRelease* durante la chiamata precedente a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) per l'utente specificato dal parametro *lpszUserName.*

Il programma di installazione per una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni nella chiave seguente nel Registro di sistema:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Per registrare la DLL, impostare i valori seguenti in questa chiave.



| Nome del valore    | Dati del valore                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Stringa **REG \_ SZ** che contiene il nome visualizzato descrittivo della DLL. |
| *DLLPath*     | Stringa **REG \_ SZ** che contiene il percorso completo della DLL.                  |



 

Ad esempio, la voce del Registro di sistema per una DLL di amministrazione RAS da una società fittizia denominata ProElectron, Inc. potrebbe essere:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **REG \_ SZ** : ProElectron RAS Admin *DLL DllPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll

Il programma di installazione per una DLL di amministrazione RAS deve inoltre fornire funzionalità di rimozione/disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del Registro di sistema della DLL.

 

 