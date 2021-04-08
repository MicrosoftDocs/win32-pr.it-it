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
# <a name="rasadminreleaseipaddress-callback-function"></a><span data-ttu-id="2abbd-104">Funzione di callback RasAdminReleaseIpAddress</span><span class="sxs-lookup"><span data-stu-id="2abbd-104">RasAdminReleaseIpAddress callback function</span></span>

<span data-ttu-id="2abbd-105">\[La funzione **RasAdminReleaseIpAddress** è disponibile per l'uso in Windows NT 4,0 e non è disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2abbd-105">\[The **RasAdminReleaseIpAddress** function is available for use in Windows NT 4.0 and is unavailable in subsequent versions.</span></span> <span data-ttu-id="2abbd-106">Usare invece [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span><span class="sxs-lookup"><span data-stu-id="2abbd-106">Instead, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span></span>

<span data-ttu-id="2abbd-107">La funzione **RasAdminReleaseIpAddress** è una funzione definita dall'applicazione che viene esportata da una DLL di amministrazione del server RAS di terze parti.</span><span class="sxs-lookup"><span data-stu-id="2abbd-107">The **RasAdminReleaseIpAddress** function is an application-defined function that is exported by a third-party RAS server administration DLL.</span></span> <span data-ttu-id="2abbd-108">RAS chiama questa funzione per notificare alla DLL che il client remoto è stato disconnesso e che l'indirizzo IP deve essere rilasciato.</span><span class="sxs-lookup"><span data-stu-id="2abbd-108">RAS calls this function to notify the DLL that the remote client was disconnected and that the IP address should be released.</span></span>

## <a name="syntax"></a><span data-ttu-id="2abbd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2abbd-109">Syntax</span></span>


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a><span data-ttu-id="2abbd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2abbd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2abbd-111">*lpszUsername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2abbd-111">*lpszUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2abbd-112">Specifica il puntatore a una stringa Unicode con terminazione null che specifica il nome di un utente remoto per il quale un indirizzo IP è stato ottenuto in precedenza utilizzando la funzione [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) .</span><span class="sxs-lookup"><span data-stu-id="2abbd-112">Specifies the pointer to a null-terminated Unicode string that specifies the name of a remote user for whom an IP address was previously obtained using the [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2abbd-113">*lpszPortName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2abbd-113">*lpszPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2abbd-114">Puntatore a una stringa Unicode con terminazione null che specifica il nome della porta su cui è connesso l'utente specificato da *lpszUsername* .</span><span class="sxs-lookup"><span data-stu-id="2abbd-114">Pointer to a null-terminated Unicode string that specifies the name of the port on which the user specified by *lpszUserName* is connected.</span></span>

</dd> <dt>

<span data-ttu-id="2abbd-115">*pipAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2abbd-115">*pipAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2abbd-116">Puntatore a una variabile **IPADDR** che specifica l'indirizzo IP restituito per l'utente in una precedente chiamata a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="2abbd-116">Pointer to an **IPADDR** variable that specifies the IP address returned for this user in a previous call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2abbd-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2abbd-117">Return value</span></span>

<span data-ttu-id="2abbd-118">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="2abbd-118">There is no extended error information for this function; do no call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="2abbd-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2abbd-119">Remarks</span></span>

<span data-ttu-id="2abbd-120">Il server RAS chiama la funzione **RasAdminReleaseIpAddress** solo se l'applicazione ha restituito **true** nel parametro *bNotifyRelease* durante la chiamata precedente a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) per l'utente specificato dal parametro *lpszUsername* .</span><span class="sxs-lookup"><span data-stu-id="2abbd-120">The RAS server calls the **RasAdminReleaseIpAddress** function only if the application returned **TRUE** in the *bNotifyRelease* parameter during the earlier call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) for the user specified by the *lpszUserName* parameter.</span></span>

<span data-ttu-id="2abbd-121">Il programma di installazione di una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni riportate nella seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="2abbd-121">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2abbd-122">Per registrare la DLL, impostare i valori seguenti in questa chiave.</span><span class="sxs-lookup"><span data-stu-id="2abbd-122">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="2abbd-123">Nome del valore</span><span class="sxs-lookup"><span data-stu-id="2abbd-123">Value name</span></span>    | <span data-ttu-id="2abbd-124">Dati del valore</span><span class="sxs-lookup"><span data-stu-id="2abbd-124">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="2abbd-125">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="2abbd-125">*DisplayName*</span></span> | <span data-ttu-id="2abbd-126">Stringa **reg \_ SZ** che contiene il nome visualizzato descrittivo della dll.</span><span class="sxs-lookup"><span data-stu-id="2abbd-126">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="2abbd-127">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="2abbd-127">*DLLPath*</span></span>     | <span data-ttu-id="2abbd-128">Stringa **reg \_ SZ** che contiene il percorso completo della dll.</span><span class="sxs-lookup"><span data-stu-id="2abbd-128">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="2abbd-129">Ad esempio, la voce del registro di sistema per una DLL di amministrazione RAS da una società fittizia denominata proelectro, Inc. potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="2abbd-129">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2abbd-130">*DisplayName*: **reg \_ SZ** : proelectron RAS admin dll *DllPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="2abbd-130">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL *DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="2abbd-131">Anche il programma di installazione di una DLL di amministrazione RAS deve fornire la funzionalità di rimozione/disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="2abbd-131">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="2abbd-132">Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del registro di sistema della DLL.</span><span class="sxs-lookup"><span data-stu-id="2abbd-132">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 