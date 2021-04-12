---
description: Per firmare un file e creare un catalogo, è necessario innanzitutto disporre di un processo per la firma di file, un certificato e una chiave pubblica.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Creazione di file e cataloghi firmati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231848"
---
# <a name="creating-signed-files-and-catalogs"></a><span data-ttu-id="5a8c5-103">Creazione di file e cataloghi firmati</span><span class="sxs-lookup"><span data-stu-id="5a8c5-103">Creating Signed Files and Catalogs</span></span>

<span data-ttu-id="5a8c5-104">Per firmare un file e creare un catalogo, è necessario innanzitutto disporre di un processo per la firma di file, un certificato e una chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="5a8c5-104">To sign a file and create a catalog for it, you must first have a process for signing files, a certificate, and a public key.</span></span>

<span data-ttu-id="5a8c5-105">**Per firmare un file e creare un catalogo**</span><span class="sxs-lookup"><span data-stu-id="5a8c5-105">**To sign a file and a create a catalog**</span></span>

1.  <span data-ttu-id="5a8c5-106">Usare [Pktextract.exe](pktextract-exe.md) per estrarre il [*token di chiave pubblica*](p-sbscs-gly.md) dal file del certificato.</span><span class="sxs-lookup"><span data-stu-id="5a8c5-106">Use [Pktextract.exe](pktextract-exe.md) to extract the [*public key token*](p-sbscs-gly.md) from the certificate file.</span></span> <span data-ttu-id="5a8c5-107">Il file del certificato deve essere presente nella stessa directory dell'utilità.</span><span class="sxs-lookup"><span data-stu-id="5a8c5-107">The certificate file must be present in the same directory as the utility.</span></span>
2.  <span data-ttu-id="5a8c5-108">Usare il valore del token di chiave pubblica per aggiornare l'attributo **PublicKeyToken** dell'elemento **assemblyIdentity** nel file manifesto.</span><span class="sxs-lookup"><span data-stu-id="5a8c5-108">Use the public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>
3.  <span data-ttu-id="5a8c5-109">Usare [MT.exe](mt-exe.md) per generare hash di file contenuti nel manifesto dell'assembly e per creare il file di descrizione del catalogo (. CDF).</span><span class="sxs-lookup"><span data-stu-id="5a8c5-109">Use [MT.exe](mt-exe.md) to generate hashes of files contained in the assembly manifest and to create the catalog description file (.cdf).</span></span>
4.  <span data-ttu-id="5a8c5-110">Utilizzare Makecat.exe con il. CDF generato per creare il catalogo di sicurezza per l'assembly.</span><span class="sxs-lookup"><span data-stu-id="5a8c5-110">Use Makecat.exe with the generated .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="5a8c5-111">Questo strumento è incluso in CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="5a8c5-111">This tool is included in the CryptoAPI.</span></span>
5.  <span data-ttu-id="5a8c5-112">Usare l'utilità [SignTool](/windows/desktop/SecCrypto/signtool) per firmare il catalogo generato con il certificato usato nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="5a8c5-112">Use the [SignTool](/windows/desktop/SecCrypto/signtool) utility to sign the catalog generated with the certificate used in step 1.</span></span> <span data-ttu-id="5a8c5-113">Il. CDF dei passaggi 3 e 4 può essere eliminato una volta creato il catalogo.</span><span class="sxs-lookup"><span data-stu-id="5a8c5-113">The .cdf from steps 3 and 4 can be deleted once the catalog is created.</span></span>

<span data-ttu-id="5a8c5-114">Vedere anche [esempio di firma degli assembly](assembly-signing-example.md).</span><span class="sxs-lookup"><span data-stu-id="5a8c5-114">See also, [Assembly Signing Example](assembly-signing-example.md).</span></span>

 

 
