---
description: In ognuna delle sezioni seguenti viene illustrata una funzione esportata da Xenroll.dll. In ogni sezione viene inoltre illustrato come utilizzare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Funzioni helper (API di registrazione certificati)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347746"
---
# <a name="helper-functions-certificate-enrollment-api"></a><span data-ttu-id="ebafd-104">Funzioni helper (API di registrazione certificati)</span><span class="sxs-lookup"><span data-stu-id="ebafd-104">Helper Functions (Certificate Enrollment API)</span></span>

<span data-ttu-id="ebafd-105">In ognuna delle sezioni seguenti viene illustrata una funzione esportata da Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="ebafd-105">Each of the following sections discusses a function exported by Xenroll.dll.</span></span> <span data-ttu-id="ebafd-106">In ogni sezione viene inoltre illustrato come utilizzare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie.</span><span class="sxs-lookup"><span data-stu-id="ebafd-106">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="binaryblobtostring"></a><span data-ttu-id="ebafd-107">binaryBlobToString</span><span class="sxs-lookup"><span data-stu-id="ebafd-107">binaryBlobToString</span></span>

<span data-ttu-id="ebafd-108">La funzione [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) in Xenroll.dll converte una matrice di byte in una stringa.</span><span class="sxs-lookup"><span data-stu-id="ebafd-108">The [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) function in Xenroll.dll converts a byte array to a string.</span></span>

<span data-ttu-id="ebafd-109">Utilizzando CertEnroll.dll, è possibile chiamare il metodo [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) sull'interfaccia [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="ebafd-109">Using CertEnroll.dll, you can call the [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="stringtobinaryblob"></a><span data-ttu-id="ebafd-110">stringToBinaryBlob</span><span class="sxs-lookup"><span data-stu-id="ebafd-110">stringToBinaryBlob</span></span>

<span data-ttu-id="ebafd-111">La funzione [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) in Xenroll.dll converte una stringa in una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="ebafd-111">The [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) function in Xenroll.dll converts a string to a byte array.</span></span>

<span data-ttu-id="ebafd-112">Utilizzando CertEnroll.dll, è possibile chiamare il metodo [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) sull'interfaccia [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="ebafd-112">Using CertEnroll.dll, you can call the [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebafd-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebafd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebafd-114">Mapping Xenroll.dll CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="ebafd-114">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="ebafd-115">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="ebafd-115">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
