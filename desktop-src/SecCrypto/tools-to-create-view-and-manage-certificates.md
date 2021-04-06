---
description: Gli strumenti CryptoAPI sono strumenti per eseguire attività comuni di gestione dei certificati.
ms.assetid: 29146de8-adae-444b-bc75-fa43a19ab8f9
title: Strumenti per creare, visualizzare e gestire i certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fb4595b7c7711b10271bd97a447a77f3a01c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759623"
---
# <a name="tools-to-create-view-and-manage-certificates"></a><span data-ttu-id="a866c-103">Strumenti per creare, visualizzare e gestire i certificati</span><span class="sxs-lookup"><span data-stu-id="a866c-103">Tools to Create, View, and Manage Certificates</span></span>

<span data-ttu-id="a866c-104">Gli strumenti CryptoAPI sono strumenti per eseguire attività comuni di gestione dei certificati.</span><span class="sxs-lookup"><span data-stu-id="a866c-104">CryptoAPI Tools are tools to perform common certificate management tasks.</span></span>



| <span data-ttu-id="a866c-105">Strumento</span><span class="sxs-lookup"><span data-stu-id="a866c-105">Tool</span></span>                                | <span data-ttu-id="a866c-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="a866c-106">Remarks</span></span>                                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a866c-107">MakeCert</span><span class="sxs-lookup"><span data-stu-id="a866c-107">MakeCert</span></span>](makecert.md)<br/> | <span data-ttu-id="a866c-108">Crea un certificato [*X. 509*](../secgloss/x-gly.md) di test.</span><span class="sxs-lookup"><span data-stu-id="a866c-108">Creates a test [*X.509*](../secgloss/x-gly.md) certificate.</span></span><br/>                                                                                |
| [<span data-ttu-id="a866c-109">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="a866c-109">Cert2SPC</span></span>](cert2spc.md)<br/> | <span data-ttu-id="a866c-110">Crea un [*certificato di autore del software*](../secgloss/s-gly.md) di test (SPC).</span><span class="sxs-lookup"><span data-stu-id="a866c-110">Creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC).</span></span><br/>           |
| [<span data-ttu-id="a866c-111">CertMgr</span><span class="sxs-lookup"><span data-stu-id="a866c-111">CertMgr</span></span>](certmgr.md)<br/>   | <span data-ttu-id="a866c-112">Gestisce certificati, scopi consentiti e [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL).</span><span class="sxs-lookup"><span data-stu-id="a866c-112">Manages certificates, CTLs, and [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs).</span></span><br/> |



 

<span data-ttu-id="a866c-113">Tutti gli input utente per questi strumenti non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a866c-113">All user input to these tools is case insensitive.</span></span> <span data-ttu-id="a866c-114">Sono ora disponibili opzioni separate per il nome della [*coppia di chiavi*](../secgloss/k-gly.md) e il file di [*chiave privata*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a866c-114">Separate options now exist for the [*key pair*](../secgloss/k-gly.md) name and the [*private key*](../secgloss/p-gly.md) file.</span></span>

## <a name="additional-tools"></a><span data-ttu-id="a866c-115">Strumenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="a866c-115">Additional Tools</span></span>

<span data-ttu-id="a866c-116">Certutil.exe è uno strumento da riga di comando che viene installato come parte di Servizi certificati.</span><span class="sxs-lookup"><span data-stu-id="a866c-116">Certutil.exe is a command-line tool that is installed as part of Certificate Services.</span></span> <span data-ttu-id="a866c-117">È possibile utilizzare Certutil.exe per eseguire il dump e visualizzare le informazioni di configurazione dell' [*autorità di certificazione*](../secgloss/c-gly.md) (CA), configurare i servizi certificati, eseguire il backup e ripristinare i componenti CA e verificare i [*certificati*](../secgloss/c-gly.md), le [*coppie di chiavi*](../secgloss/k-gly.md)e le catene di certificati.</span><span class="sxs-lookup"><span data-stu-id="a866c-117">You can use Certutil.exe to dump and display [*certification authority*](../secgloss/c-gly.md) (CA) configuration information, configure Certificate Services, back up and restore CA components, and verify [*certificates*](../secgloss/c-gly.md), [*key pairs*](../secgloss/k-gly.md), and certificate chains.</span></span> <span data-ttu-id="a866c-118">Per ulteriori informazioni su Certutil, vedere l'argomento [certutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732443(v=ws.11)) in Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="a866c-118">For more information about Certutil, see the [Certutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732443(v=ws.11)) topic on Microsoft TechNet.</span></span>

 

 
