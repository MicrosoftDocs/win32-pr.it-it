---
description: ICE81 convalida la tabella MsiDigitalCertificate, la tabella MsiDigitalSignature, la tabella MsiPatchCertificate e la tabella MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752791"
---
# <a name="ice81"></a><span data-ttu-id="7daf9-103">ICE81</span><span class="sxs-lookup"><span data-stu-id="7daf9-103">ICE81</span></span>

<span data-ttu-id="7daf9-104">ICE81 convalida la tabella [MsiDigitalCertificate](msidigitalcertificate-table.md), la tabella [MsiDigitalSignature](msidigitalsignature-table.md), la tabella [MsiPatchCertificate](msipatchcertificate-table.md)e la [tabella MsiPackageCertificate](msipackagecertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="7daf9-104">ICE81 validates the [MsiDigitalCertificate table](msidigitalcertificate-table.md), [MsiDigitalSignature table](msidigitalsignature-table.md), [MsiPatchCertificate table](msipatchcertificate-table.md), and [MsiPackageCertificate Table](msipackagecertificate-table.md).</span></span> <span data-ttu-id="7daf9-105">Questa azione personalizzata del ghiaccio invia avvisi per i certificati digitali non usati o senza riferimenti e invia un errore quando l'oggetto firmato non esiste o quando il cabinet dell'oggetto firmato non punta a dati esterni.</span><span class="sxs-lookup"><span data-stu-id="7daf9-105">This ICE custom action posts warnings for digital certificates that are unused or unreferenced, and it posts an error when the signed object does not exist or when the signed object's cabinet does not point to external data.</span></span>

<span data-ttu-id="7daf9-106">Si noti che ICE03 verifica che la voce nella colonna della tabella nella tabella MsiDigitalSignature sia "media".</span><span class="sxs-lookup"><span data-stu-id="7daf9-106">Note that ICE03 verifies that the entry in the Table column in the MsiDigitalSignature table is "Media."</span></span>

## <a name="result"></a><span data-ttu-id="7daf9-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="7daf9-107">Result</span></span>

<span data-ttu-id="7daf9-108">ICE81 invia gli avvisi seguenti per i certificati digitali non usati o senza riferimenti.</span><span class="sxs-lookup"><span data-stu-id="7daf9-108">ICE81 posts the following warnings for unused or unreferenced Digital Certificates.</span></span>



| <span data-ttu-id="7daf9-109">Avviso di ICE81</span><span class="sxs-lookup"><span data-stu-id="7daf9-109">ICE81 warning</span></span>                                                                                                                                                      | <span data-ttu-id="7daf9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7daf9-110">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7daf9-111">Nessun riferimento a nessuno dei record nella tabella MsiDigitalCertificate è stato trovato nelle tabelle MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="7daf9-111">No reference to any of the records in the MsiDigitalCertificate table could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span> | <span data-ttu-id="7daf9-112">Questo avviso viene restituito se tutti i record non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="7daf9-112">This warning is returned if all records are unused.</span></span>                |
| <span data-ttu-id="7daf9-113">Nessun riferimento al certificato digitale \[ 1 \] è stato trovato nelle tabelle MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="7daf9-113">No reference to the Digital Certificate \[1\] could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span>                         | <span data-ttu-id="7daf9-114">Questo avviso viene restituito se alcuni record, ma non tutti, non sono utilizzati.</span><span class="sxs-lookup"><span data-stu-id="7daf9-114">This warning is returned if some records, but not all, are unused.</span></span> |



 

<span data-ttu-id="7daf9-115">ICE81 invia i seguenti errori.</span><span class="sxs-lookup"><span data-stu-id="7daf9-115">ICE81 posts the following errors.</span></span>



| <span data-ttu-id="7daf9-116">Errore ICE81</span><span class="sxs-lookup"><span data-stu-id="7daf9-116">ICE81 error</span></span>                                                                                                                                                              | <span data-ttu-id="7daf9-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7daf9-117">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7daf9-118">La tabella supporti non esiste.</span><span class="sxs-lookup"><span data-stu-id="7daf9-118">Media Table does not exist.</span></span> <span data-ttu-id="7daf9-119">Di conseguenza, tutte le voci in MsiDigitalSignature non sono corrette</span><span class="sxs-lookup"><span data-stu-id="7daf9-119">Hence all the entries in MsiDigitalSignature are incorrect</span></span>                                                                                   | <span data-ttu-id="7daf9-120">L'oggetto firmato non esiste.</span><span class="sxs-lookup"><span data-stu-id="7daf9-120">The signed object does not exist.</span></span> <span data-ttu-id="7daf9-121">Questo errore viene restituito se la tabella dei supporti non esiste ma MsiDigitalSignature contiene voci.</span><span class="sxs-lookup"><span data-stu-id="7daf9-121">This error is returned if the Media table does not exist but MsiDigitalSignature has entries.</span></span>                                |
| <span data-ttu-id="7daf9-122">Oggetto firmato mancante \[ 2 \] nella tabella supporti</span><span class="sxs-lookup"><span data-stu-id="7daf9-122">Missing signed object \[2\] in Media Table</span></span>                                                                                                                               | <span data-ttu-id="7daf9-123">L'oggetto firmato \[ 2 non \] esiste.</span><span class="sxs-lookup"><span data-stu-id="7daf9-123">The signed object \[2\] does not exist.</span></span> <span data-ttu-id="7daf9-124">Questo errore viene restituito se la tabella supporti esiste, ma questa voce in MsiDigitalSignature non è presente nella tabella dei supporti.</span><span class="sxs-lookup"><span data-stu-id="7daf9-124">This error is returned if the Media table exists, but this entry in MsiDigitalSignature is not present in Media table.</span></span> |
| <span data-ttu-id="7daf9-125">La voce nella tabella \[ 1 \] con chiave \[ 2 \] è firmata.</span><span class="sxs-lookup"><span data-stu-id="7daf9-125">The entry in table \[1\] with key \[2\] is signed.</span></span> <span data-ttu-id="7daf9-126">Il cabinet deve quindi puntare a un oggetto all'esterno del pacchetto (il valore del file CAB non deve essere preceduto da \# )</span><span class="sxs-lookup"><span data-stu-id="7daf9-126">Hence the cabinet should point to an object outside the package (the value of Cabinet should NOT be prefixed with \#)</span></span> | <span data-ttu-id="7daf9-127">Il cabinet dell'oggetto firmato non punta a dati esterni.</span><span class="sxs-lookup"><span data-stu-id="7daf9-127">The signed object's cabinet does not point to external data.</span></span> <span data-ttu-id="7daf9-128">\[1 \] è il nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="7daf9-128">\[1\] is table name.</span></span> <span data-ttu-id="7daf9-129">\[2 \] è la chiave nella tabella dei supporti.</span><span class="sxs-lookup"><span data-stu-id="7daf9-129">\[2\] is key in the Media table.</span></span>                                             |



 

## <a name="related-topics"></a><span data-ttu-id="7daf9-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7daf9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7daf9-131">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="7daf9-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



