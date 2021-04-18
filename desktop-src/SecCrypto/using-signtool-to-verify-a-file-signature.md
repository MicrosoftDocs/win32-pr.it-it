---
description: Viene illustrato come utilizzare SignTool per verificare una firma del file.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Uso di SignTool per verificare una firma del file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8161d4c890400f3aa33b415e7ac16a5306aa094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308629"
---
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="5676c-103">Uso di SignTool per verificare una firma del file</span><span class="sxs-lookup"><span data-stu-id="5676c-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="5676c-104">Il comando seguente verifica la firma di un file denominato *MyControl.exe*:</span><span class="sxs-lookup"><span data-stu-id="5676c-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="5676c-105">**Verifica** *MyControl.exe* di SignTool</span><span class="sxs-lookup"><span data-stu-id="5676c-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="5676c-106">Se l'esempio precedente ha esito negativo, è possibile che la firma abbia utilizzato un certificato di firma codice.</span><span class="sxs-lookup"><span data-stu-id="5676c-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="5676c-107">Per impostazione predefinita, [SignTool](signtool.md) è il criterio driver di Windows per la verifica.</span><span class="sxs-lookup"><span data-stu-id="5676c-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="5676c-108">Il comando seguente verifica la firma, usando i criteri di verifica dell'autenticazione predefiniti:</span><span class="sxs-lookup"><span data-stu-id="5676c-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="5676c-109">**SignTool Verify/pa** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="5676c-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="5676c-110">Il comando seguente verifica un file di sistema che può essere firmato in un catalogo:</span><span class="sxs-lookup"><span data-stu-id="5676c-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="5676c-111">**Verifica di SignTool/a** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="5676c-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="5676c-112">Il comando seguente verifica un file di sistema firmato in un catalogo denominato *MyCat.cat*:</span><span class="sxs-lookup"><span data-stu-id="5676c-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="5676c-113">**Verifica di SignTool/c** *MyCat.catMyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="5676c-113">**SignTool verify /c** *MyCat.catMyFile.ini*</span></span>

<span data-ttu-id="5676c-114">Per qualsiasi verifica di [SignTool](signtool.md) , è possibile recuperare il firmatario del certificato.</span><span class="sxs-lookup"><span data-stu-id="5676c-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="5676c-115">Il comando seguente verifica un file di sistema e visualizza il certificato del firmatario:</span><span class="sxs-lookup"><span data-stu-id="5676c-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="5676c-116">**Verifica di SignTool** *MyControl.exe* /v</span><span class="sxs-lookup"><span data-stu-id="5676c-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="5676c-117">[SignTool](signtool.md) restituisce il testo della riga di comando che indica il risultato del controllo della firma.</span><span class="sxs-lookup"><span data-stu-id="5676c-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="5676c-118">Inoltre, SignTool restituisce un codice di uscita pari a zero per l'esecuzione completata, uno per l'esecuzione non riuscita e due per l'esecuzione completata con avvisi.</span><span class="sxs-lookup"><span data-stu-id="5676c-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="5676c-119">Per ulteriori informazioni su [SignTool](signtool.md), vedere [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="5676c-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



