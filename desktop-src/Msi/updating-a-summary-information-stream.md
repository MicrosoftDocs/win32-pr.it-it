---
description: Il valore della proprietà riepilogo Numero revisione nel flusso di informazioni di riepilogo deve essere modificato in un nuovo valore univoco durante la localizzazione di un database, perché è in corso la modifica del database di installazione. Vedere codici di pacchetto.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Aggiornamento di un flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401785"
---
# <a name="updating-a-summary-information-stream"></a><span data-ttu-id="6ecc8-104">Aggiornamento di un flusso di informazioni di riepilogo</span><span class="sxs-lookup"><span data-stu-id="6ecc8-104">Updating a Summary Information Stream</span></span>

<span data-ttu-id="6ecc8-105">Il valore della proprietà [**Riepilogo numero revisione**](revision-number-summary.md) nel flusso di [informazioni di riepilogo](summary-information-stream.md) deve essere modificato in un nuovo valore univoco durante la localizzazione di un database, perché è in corso la modifica del database di installazione.</span><span class="sxs-lookup"><span data-stu-id="6ecc8-105">The value of the [**Revision Number Summary**](revision-number-summary.md) Property in the [summary information stream](summary-information-stream.md) must be changed to a new, unique value when localizing a database, because the installation database is being changed.</span></span> <span data-ttu-id="6ecc8-106">Vedere [codici di pacchetto](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6ecc8-106">See [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="6ecc8-107">Il valore della proprietà di [**Riepilogo del modello**](template-summary.md) nel flusso di informazioni di riepilogo deve essere modificato in LangID (numeric Language Identifier) del nuovo linguaggio.</span><span class="sxs-lookup"><span data-stu-id="6ecc8-107">The value of the [**Template Summary**](template-summary.md) Property in the summary information stream must be changed to the numeric language identifier (LANGID) of the new language.</span></span>

<span data-ttu-id="6ecc8-108">Se le stringhe di testo descrittivo nel flusso di informazioni di riepilogo sono localizzate nel nuovo linguaggio, è necessario impostare la proprietà di [**Riepilogo codepage**](codepage-summary.md) sulla tabella codici corretta per il nuovo linguaggio.</span><span class="sxs-lookup"><span data-stu-id="6ecc8-108">If the descriptive text strings in the summary information stream are localized to the new language, the [**Codepage Summary**](codepage-summary.md) Property must be set to the correct code page for the new language.</span></span>

<span data-ttu-id="6ecc8-109">È possibile modificare il flusso di informazioni di riepilogo del pacchetto localizzato con la stessa procedura descritta in [aggiunta di informazioni di riepilogo](adding-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="6ecc8-109">You may modify the summary information stream of the localized package by the same procedure as in [Adding Summary Information](adding-summary-information.md).</span></span> <span data-ttu-id="6ecc8-110">Un esempio che illustra l'uso dei metodi di informazioni di riepilogo del database viene fornito anche in Windows Installer SDK come WiSumInf.vbs di utilità.</span><span class="sxs-lookup"><span data-stu-id="6ecc8-110">An example demonstrating the use of the database summary information methods is also provided in the Windows Installer SDK as the utility WiSumInf.vbs.</span></span> <span data-ttu-id="6ecc8-111">Per ulteriori informazioni su WiSumInf.vbs, vedere [gestione delle informazioni di riepilogo](manage-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="6ecc8-111">For more information about WiSumInf.vbs, see [Manage Summary Information](manage-summary-information.md).</span></span>

[<span data-ttu-id="6ecc8-112">Continua</span><span class="sxs-lookup"><span data-stu-id="6ecc8-112">Continue</span></span>](adding-localized-resources.md)

 

 



