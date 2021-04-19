---
description: Il metodo SetEncryptionKey imposta la chiave di crittografia necessaria per decrittografare la sessione o un'indicazione in un meccanismo per ottenere una chiave utilizzabile per mezzo esterno.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'Metodo ITConnection:: SetEncryptionKey (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326492"
---
# <a name="itconnectionsetencryptionkey-method"></a><span data-ttu-id="a9ae6-103">Metodo ITConnection:: SetEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a9ae6-103">ITConnection::SetEncryptionKey method</span></span>

<span data-ttu-id="a9ae6-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a9ae6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a9ae6-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a9ae6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a9ae6-106">Il metodo **SetEncryptionKey** imposta la chiave di crittografia necessaria per decrittografare la sessione o un'indicazione in un meccanismo per ottenere una chiave utilizzabile per mezzo esterno.</span><span class="sxs-lookup"><span data-stu-id="a9ae6-106">The **SetEncryptionKey** method sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ae6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9ae6-107">Syntax</span></span>


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="a9ae6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9ae6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ae6-109">*pKeyType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9ae6-109">*pKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ae6-110">Puntatore a un **BSTR** che contiene il tipo di chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="a9ae6-110">Pointer to a **BSTR** containing the encryption key type.</span></span>

</dd> <dt>

<span data-ttu-id="a9ae6-111">*ppKeyData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9ae6-111">*ppKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ae6-112">Puntatore a un **BSTR** contenente le informazioni sulla chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="a9ae6-112">Pointer to a **BSTR** containing encryption key information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ae6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9ae6-113">Return value</span></span>

<span data-ttu-id="a9ae6-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a9ae6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a9ae6-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a9ae6-115">Return code</span></span>                                                                          | <span data-ttu-id="a9ae6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9ae6-116">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="a9ae6-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9ae6-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a9ae6-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a9ae6-118">Method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9ae6-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9ae6-119">Remarks</span></span>

<span data-ttu-id="a9ae6-120">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per i parametri *pKeyType* e *ppKeyData* .</span><span class="sxs-lookup"><span data-stu-id="a9ae6-120">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pKeyType* and *ppKeyData* parameters.</span></span> <span data-ttu-id="a9ae6-121">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando le variabili non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="a9ae6-121">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ae6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9ae6-122">Requirements</span></span>



| <span data-ttu-id="a9ae6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ae6-123">Requirement</span></span> | <span data-ttu-id="a9ae6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a9ae6-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ae6-125">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a9ae6-125">TAPI version</span></span><br/> | <span data-ttu-id="a9ae6-126">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a9ae6-126">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a9ae6-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9ae6-127">Header</span></span><br/>       | <dl> <span data-ttu-id="a9ae6-128"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9ae6-128"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9ae6-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9ae6-129">Library</span></span><br/>      | <dl> <span data-ttu-id="a9ae6-130"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9ae6-130"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a9ae6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a9ae6-131">DLL</span></span><br/>          | <dl> <span data-ttu-id="a9ae6-132"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9ae6-132"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ae6-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9ae6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ae6-134">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="a9ae6-134">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

