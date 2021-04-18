---
description: La progettazione di SSPI consente la scrittura e l'aggiunta di SSP aggiuntivi al sistema.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Scrittura e installazione di un Security Support Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313726"
---
# <a name="writing-and-installing-a-security-support-provider"></a><span data-ttu-id="1980d-103">Scrittura e installazione di un Security Support Provider</span><span class="sxs-lookup"><span data-stu-id="1980d-103">Writing and Installing a Security Support Provider</span></span>

<span data-ttu-id="1980d-104">La progettazione di SSPI consente la scrittura e l'aggiunta di SSP aggiuntivi al sistema.</span><span class="sxs-lookup"><span data-stu-id="1980d-104">The design of SSPI enables additional SSPs to be written and added to the system.</span></span> <span data-ttu-id="1980d-105">Un [*SSP*](../secgloss/s-gly.md) specifico di un modello di sicurezza può essere sviluppato con la relativa semplicità o complessità elevata, a seconda del livello di integrazione con il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1980d-105">An [*SSP*](../secgloss/s-gly.md) specific to a security model can be developed with relative ease or great complexity, depending on the level of integration with the operating system.</span></span> <span data-ttu-id="1980d-106">Un SSP client che consente di stabilire connessioni a un nuovo tipo di server può essere sviluppato molto rapidamente, mentre un SSP completo che fornisce la rappresentazione locale richiederebbe maggiore sforzo.</span><span class="sxs-lookup"><span data-stu-id="1980d-106">A client SSP that allows connections to a new type of server could be developed very quickly, whereas a full SSP that provides local impersonation would require more effort.</span></span>

<span data-ttu-id="1980d-107">I provider di servizi condivisi vengono installati aggiornando un valore **reg \_ SZ** nel registro di sistema, disponibile nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="1980d-107">SSPs are installed by updating a **REG\_SZ** value in the registry, located as follows:</span></span>

<span data-ttu-id="1980d-108">**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    </span><span class="sxs-lookup"><span data-stu-id="1980d-108">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **SecurityProviders** = *Provider1.dll, Provider2.dll,*…</span></span><dl> <dt>

            Data type
</dt> <dd>            <span data-ttu-id="1980d-109">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1980d-109">REG\_SZ</span></span></dd> </dl>

<span data-ttu-id="1980d-110">Una singola DLL può contenere più SSP.</span><span class="sxs-lookup"><span data-stu-id="1980d-110">A single DLL can contain multiple SSPs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1980d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1980d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1980d-112">Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza</span><span class="sxs-lookup"><span data-stu-id="1980d-112">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
