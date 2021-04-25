---
description: Illustra come usare SignTool per verificare la firma di un file.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Uso di SignTool per verificare la firma di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e91df7a64a8db48d04ceba9df5fbc3fd358058
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954924"
---
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="b6e91-103">Uso di SignTool per verificare la firma di un file</span><span class="sxs-lookup"><span data-stu-id="b6e91-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="b6e91-104">Il comando seguente verifica la firma di un file *denominatoMyControl.exe*:</span><span class="sxs-lookup"><span data-stu-id="b6e91-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="b6e91-105">**Verifica signTool** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="b6e91-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="b6e91-106">Se l'esempio precedente ha esito negativo, la firma potrebbe usare un certificato di firma del codice.</span><span class="sxs-lookup"><span data-stu-id="b6e91-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="b6e91-107">[Per impostazione predefinita, SignTool](signtool.md) fa riferimento ai criteri del driver Windows per la verifica.</span><span class="sxs-lookup"><span data-stu-id="b6e91-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="b6e91-108">Il comando seguente verifica la firma usando i criteri di verifica dell'autenticazione predefiniti:</span><span class="sxs-lookup"><span data-stu-id="b6e91-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="b6e91-109">**SignTool verify /pa** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="b6e91-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="b6e91-110">Il comando seguente verifica un file di sistema che può essere firmato in un catalogo:</span><span class="sxs-lookup"><span data-stu-id="b6e91-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="b6e91-111">**Verifica SignTool /a** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="b6e91-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="b6e91-112">Il comando seguente verifica un file di sistema firmato in un catalogo denominato *MyCat.cat*:</span><span class="sxs-lookup"><span data-stu-id="b6e91-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="b6e91-113">**SignTool verify /c** *MyCat.cat* *MyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="b6e91-113">**SignTool verify /c** *MyCat.cat* *MyFile.ini*</span></span>

<span data-ttu-id="b6e91-114">Per qualsiasi [verifica SignTool,](signtool.md) è possibile recuperare il firmatario del certificato.</span><span class="sxs-lookup"><span data-stu-id="b6e91-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="b6e91-115">Il comando seguente verifica un file di sistema e visualizza il certificato del firmatario:</span><span class="sxs-lookup"><span data-stu-id="b6e91-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="b6e91-116">**SignTool verify /v** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="b6e91-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="b6e91-117">[SignTool](signtool.md) restituisce il testo della riga di comando che indica il risultato del controllo della firma.</span><span class="sxs-lookup"><span data-stu-id="b6e91-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="b6e91-118">SignTool restituisce inoltre un codice di uscita pari a zero per l'esecuzione riuscita, uno per l'esecuzione non riuscita e due per l'esecuzione completata con avvisi.</span><span class="sxs-lookup"><span data-stu-id="b6e91-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="b6e91-119">Per altre informazioni su [SignTool,](signtool.md)vedere [SignTool.](signtool.md)</span><span class="sxs-lookup"><span data-stu-id="b6e91-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



