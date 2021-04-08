---
title: Funzione di callback RasAdminReleaseIpAddress
description: La funzione RasAdminReleaseIpAddress è una funzione definita dall'applicazione che viene esportata da una DLL di amministrazione del server RAS di terze parti.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- RAS funzione di callback RasAdminReleaseIpAddress
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729815"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>Funzione di callback RasAdminReleaseIpAddress

\[La funzione **RasAdminReleaseIpAddress** è disponibile per l'uso in Windows NT 4,0 e non è disponibile nelle versioni successive. Usare invece [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]

La funzione **RasAdminReleaseIpAddress** è una funzione definita dall'applicazione che viene esportata da una DLL di amministrazione del server RAS di terze parti. RAS chiama questa funzione per notificare alla DLL che il client remoto è stato disconnesso e che l'indirizzo IP deve essere rilasciato.

## <a name="syntax"></a>Sintassi


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszUsername* \[ in\]
</dt> <dd>

Specifica il puntatore a una stringa Unicode con terminazione null che specifica il nome di un utente remoto per il quale un indirizzo IP è stato ottenuto in precedenza utilizzando la funzione [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) .

</dd> <dt>

*lpszPortName* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome della porta su cui è connesso l'utente specificato da *lpszUsername* .

</dd> <dt>

*pipAddress* \[ in\]
</dt> <dd>

Puntatore a una variabile **IPADDR** che specifica l'indirizzo IP restituito per l'utente in una precedente chiamata a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Il server RAS chiama la funzione **RasAdminReleaseIpAddress** solo se l'applicazione ha restituito **true** nel parametro *bNotifyRelease* durante la chiamata precedente a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) per l'utente specificato dal parametro *lpszUsername* .

Il programma di installazione di una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni riportate nella seguente chiave del registro di sistema:

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
| *DisplayName* | Stringa **reg \_ SZ** che contiene il nome visualizzato descrittivo della dll. |
| *DLLPath*     | Stringa **reg \_ SZ** che contiene il percorso completo della dll.                  |



 

Ad esempio, la voce del registro di sistema per una DLL di amministrazione RAS da una società fittizia denominata proelectro, Inc. potrebbe essere:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **reg \_ SZ** : proelectron RAS admin dll *DllPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll

Anche il programma di installazione di una DLL di amministrazione RAS deve fornire la funzionalità di rimozione/disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del registro di sistema della DLL.

 

 