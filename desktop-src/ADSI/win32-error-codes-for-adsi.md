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
# <a name="win32-error-codes-for-adsi"></a><span data-ttu-id="b6ebc-104">Codici di errore Win32 per ADSI</span><span class="sxs-lookup"><span data-stu-id="b6ebc-104">Win32 Error Codes for ADSI</span></span>

<span data-ttu-id="b6ebc-105">I codici di errore Win32 standard vengono inoltre utilizzati per restituire messaggi di errore ADSI.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-105">Standard Win32 error codes are also used to return ADSI error messages.</span></span> <span data-ttu-id="b6ebc-106">In particolare, il provider LDAP ADSI esegue il mapping di tutti i codici di errore LDAP ai codici di errore Win32.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-106">Specifically, the ADSI LDAP provider maps all the LDAP error codes to Win32 error codes.</span></span> <span data-ttu-id="b6ebc-107">I valori **HRESULT** di questi codici di errore sono del formato 0x8007XXXX, dove le ultime quattro cifre esadecimali, xxxx, corrispondono ai valori **DWORD** del codice di errore Win32 appropriato.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-107">The **HRESULT** values of these error codes are of the 0x8007XXXX format, where the last four hexadecimal digits, XXXX, corresponds to the **DWORD** values of the appropriate Win32 error code.</span></span> <span data-ttu-id="b6ebc-108">Il valore di errore ADSI 0x80072020, ad esempio, restituisce il valore di errore Win32 di 0x2020 in formato esadecimale o 8224 in decimale.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-108">For example, the ADSI error value 0x80072020 gives the Win32 error value of 0x2020 in hexadecimal or 8224 in decimal.</span></span>

<span data-ttu-id="b6ebc-109">Per convertire il valore **HRESULT** di un codice di errore ADSI, restituito dall'applicazione, nel valore **DWORD** dell'errore Win32 corrispondente, come definito nei file di intestazione precedenti, utilizzare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-109">To convert the **HRESULT** value of an ADSI error code, returned by your application, to the corresponding the Win32 error **DWORD** value, as defined in the header files above, use the following procedure.</span></span>

<span data-ttu-id="b6ebc-110">La maggior parte dei codici di errore Win32 per ADSI è definita in Winerror. h o Lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-110">Most of the Win32 error codes for ADSI are defined in Winerror.h or Lmerr.h.</span></span> <span data-ttu-id="b6ebc-111">I valori di errore sono elencati come valori decimali in questi file.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-111">The error values are listed as decimal values in these files.</span></span>

<span data-ttu-id="b6ebc-112">**Per convertire il valore **HRESULT** di un codice di errore ADSI nel valore **DWORD** dell'errore Win32 corrispondente**</span><span class="sxs-lookup"><span data-stu-id="b6ebc-112">**To convert the **HRESULT** value of an ADSI error code to the corresponding the Win32 error **DWORD** value**</span></span>

1.  <span data-ttu-id="b6ebc-113">Convertire il valore **HRESULT** in un numero esadecimale se si inizia con un valore decimale, come si può ottenere da un'applicazione Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-113">Convert the **HRESULT** value to a hexadecimal number if starting with a decimal value as you may get from a Visual Basic application.</span></span>
2.  <span data-ttu-id="b6ebc-114">Rilasciare la parte 0x8007 per produrre il resto.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-114">Drop the 0x8007 part produce the remainder.</span></span>
3.  <span data-ttu-id="b6ebc-115">Converte il resto in un numero decimale.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-115">Convert the remainder to a decimal number.</span></span>
4.  <span data-ttu-id="b6ebc-116">Cercare il resto decimale in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-116">Look up the decimal remainder in Winerror.h.</span></span>
5.  <span data-ttu-id="b6ebc-117">Se non viene trovato in Winerror. h, sottrarre 2100 dal resto decimale e cercare il risultato in Lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-117">If not found in Winerror.h, subtract 2100 from the decimal remainder and look up the result in Lmerr.h.</span></span>

<span data-ttu-id="b6ebc-118">ADSI 2,0 esegue il mapping dei codici di errore LDAP a un set di codici di errore Win32 diverso da quello usato in ADSI per Windows 2000 e il client DS.</span><span class="sxs-lookup"><span data-stu-id="b6ebc-118">ADSI 2.0 maps the LDAP error codes to a set of Win32 error codes that is different from that used in ADSI for Windows 2000 and DS Client.</span></span> <span data-ttu-id="b6ebc-119">Le differenze sono elencate in:</span><span class="sxs-lookup"><span data-stu-id="b6ebc-119">The differences are listed in:</span></span>

-   [<span data-ttu-id="b6ebc-120">Codici di errore Win32</span><span class="sxs-lookup"><span data-stu-id="b6ebc-120">Win32 Error Codes</span></span>](win32-error-codes.md)
-   [<span data-ttu-id="b6ebc-121">Codici di errore Win32 per ADSI 2,0</span><span class="sxs-lookup"><span data-stu-id="b6ebc-121">Win32 Error Codes for ADSI 2.0</span></span>](win32-error-codes-for-adsi-2-0.md)

 

 




