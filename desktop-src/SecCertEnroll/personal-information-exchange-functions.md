---
description: In ognuna delle sezioni seguenti viene illustrata una funzione esportata da Xenroll.dll per gestire i messaggi PFX (Personal Information Exchange).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funzioni scambio informazioni personali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315396"
---
# <a name="personal-information-exchange-functions"></a><span data-ttu-id="7d116-103">Funzioni scambio informazioni personali</span><span class="sxs-lookup"><span data-stu-id="7d116-103">Personal Information Exchange Functions</span></span>

<span data-ttu-id="7d116-104">In ognuna delle sezioni seguenti viene illustrata una funzione esportata da Xenroll.dll per gestire i messaggi PFX (Personal Information Exchange).</span><span class="sxs-lookup"><span data-stu-id="7d116-104">Each of the following sections discusses a function exported by Xenroll.dll to manage Personal Information Exchange (PFX) messages.</span></span> <span data-ttu-id="7d116-105">In ogni sezione viene inoltre illustrato come utilizzare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie.</span><span class="sxs-lookup"><span data-stu-id="7d116-105">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="createfilepfxwstr"></a><span data-ttu-id="7d116-106">createFilePFXWStr</span><span class="sxs-lookup"><span data-stu-id="7d116-106">createFilePFXWStr</span></span>

<span data-ttu-id="7d116-107">La funzione [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) in Xenroll.dll salva una catena di certificati e una [*chiave privata*](/windows/desktop/SecGloss/p-gly) in un file usando il formato pfx.</span><span class="sxs-lookup"><span data-stu-id="7d116-107">The [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) function in Xenroll.dll saves a certificate chain and [*private key*](/windows/desktop/SecGloss/p-gly) in a file by using the PFX format.</span></span>

<span data-ttu-id="7d116-108">La libreria CertEnroll.dll non implementa direttamente le funzionalità per copiare il messaggio PFX in un file.</span><span class="sxs-lookup"><span data-stu-id="7d116-108">The CertEnroll.dll library does not directly implement functionality to copy the PFX message to a file.</span></span> <span data-ttu-id="7d116-109">È tuttavia possibile utilizzare il metodo [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) sull'interfaccia [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per creare un messaggio PFX codificato e scrivere una funzione personalizzata per salvare il messaggio in un file.</span><span class="sxs-lookup"><span data-stu-id="7d116-109">You can, however, use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message and write a custom function to save the message in a file.</span></span>

## <a name="createpfxwstr"></a><span data-ttu-id="7d116-110">createPFXWStr</span><span class="sxs-lookup"><span data-stu-id="7d116-110">createPFXWStr</span></span>

<span data-ttu-id="7d116-111">La funzione [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) in Xenroll.dll salva una catena di certificati e una chiave privata in una stringa di formato pfx.</span><span class="sxs-lookup"><span data-stu-id="7d116-111">The [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) function in Xenroll.dll saves a certificate chain and private key in a PFX format string.</span></span>

<span data-ttu-id="7d116-112">È possibile usare il metodo [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) sull'interfaccia [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per creare un messaggio PFX codificato che contiene la catena di certificati e la chiave.</span><span class="sxs-lookup"><span data-stu-id="7d116-112">You can use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message that contains the certificate chain and key.</span></span> <span data-ttu-id="7d116-113">È possibile specificare una password, le opzioni di esportazione e il tipo di codifica.</span><span class="sxs-lookup"><span data-stu-id="7d116-113">You can specify a password, export options, and encoding type.</span></span> <span data-ttu-id="7d116-114">Per recuperare una stringa equivalente a quella restituita da [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), passare il flag XCN \_ crypt \_ String \_ Binary nell'oggetto nel parametro *Encoding* del metodo [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .</span><span class="sxs-lookup"><span data-stu-id="7d116-114">To retrieve a string that is equivalent to that returned from [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pass the XCN\_CRYPT\_STRING\_BINARY flag in the in the *Encoding* parameter of the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d116-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d116-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d116-116">Mapping Xenroll.dll CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="7d116-116">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="7d116-117">**Metodo IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="7d116-117">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
