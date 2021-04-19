---
description: Viene usato come handle per un provider del servizio di crittografia (CSP) CryptoAPI o un CSP CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316155"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a><span data-ttu-id="99820-103">\_handle di chiave HCRYPTPROV o \_ NCRYPT \_ \_</span><span class="sxs-lookup"><span data-stu-id="99820-103">HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE</span></span>

<span data-ttu-id="99820-104">Il tipo di dati dell' **handle di \_ chiave HCRYPTPROV o \_ NCRYPT \_ \_** viene usato come handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) CryptoAPI o un CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="99820-104">The **HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE** data type is used as a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> <span data-ttu-id="99820-105">Questo handle deve essere un handle [**HCRYPTPROV**](hcryptprov.md) creato tramite la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) o un handle di **\_ \_ handle di chiave NCRYPT** creato utilizzando la funzione [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) .</span><span class="sxs-lookup"><span data-stu-id="99820-105">This handle must be an [**HCRYPTPROV**](hcryptprov.md) handle that has been created by using the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function or an **NCRYPT\_KEY\_HANDLE** handle that has been created by using the [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) function.</span></span> <span data-ttu-id="99820-106">Le nuove applicazioni devono sempre passare l'handle della **\_ \_ chiave NCRYPT** a un CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="99820-106">New applications should always pass in the **NCRYPT\_KEY\_HANDLE** handle to a CNG CSP.</span></span>


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="99820-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99820-107">Requirements</span></span>



| <span data-ttu-id="99820-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="99820-108">Requirement</span></span> | <span data-ttu-id="99820-109">Valore</span><span class="sxs-lookup"><span data-stu-id="99820-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99820-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99820-110">Minimum supported client</span></span><br/> | <span data-ttu-id="99820-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99820-111">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99820-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99820-112">Minimum supported server</span></span><br/> | <span data-ttu-id="99820-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99820-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99820-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99820-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="99820-115"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="99820-115"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
