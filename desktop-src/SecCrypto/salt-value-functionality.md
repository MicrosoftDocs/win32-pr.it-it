---
description: Il provider di base crea chiavi simmetriche a 40 bit create con undici byte di Salt di valore zero, undici byte di Salt diverso da zero \_ se \_ è specificato Crypt create Salt o nessun valore salt.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Funzionalità valore Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344346"
---
# <a name="salt-value-functionality"></a><span data-ttu-id="939fd-103">Funzionalità valore Salt</span><span class="sxs-lookup"><span data-stu-id="939fd-103">Salt Value Functionality</span></span>

<span data-ttu-id="939fd-104">Il provider di base crea [*chiavi simmetriche*](../secgloss/s-gly.md) a 40 bit create con undici byte di [*Salt*](../secgloss/s-gly.md)di valore zero, undici byte di Salt diverso da zero \_ se \_ è specificato Crypt create Salt o nessun valore salt.</span><span class="sxs-lookup"><span data-stu-id="939fd-104">The Base Provider creates 40-bit [*symmetric keys*](../secgloss/s-gly.md) created with eleven bytes of zero-value [*salt*](../secgloss/s-gly.md), eleven bytes of nonzero salt if CRYPT\_CREATE\_SALT is specified, or no salt value.</span></span> <span data-ttu-id="939fd-105">Una chiave simmetrica a 40 bit con Salt con valore zero, tuttavia, non è equivalente a una chiave simmetrica a 40 bit senza Salt.</span><span class="sxs-lookup"><span data-stu-id="939fd-105">A 40-bit symmetric key with zero-value salt, however, is not equivalent to a 40-bit symmetric key without salt.</span></span> <span data-ttu-id="939fd-106">Per l'interoperabilità, è necessario creare chiavi senza Salt.</span><span class="sxs-lookup"><span data-stu-id="939fd-106">For interoperability, keys must be created without salt.</span></span> <span data-ttu-id="939fd-107">Questo problema deriva da una condizione predefinita che si verifica solo con chiavi di esattamente 40 bit.</span><span class="sxs-lookup"><span data-stu-id="939fd-107">This problem results from a default condition that occurs only with keys of exactly 40 bits.</span></span> <span data-ttu-id="939fd-108">Tutte le altre [*lunghezze di chiave*](../secgloss/k-gly.md) non hanno allocato Salt per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="939fd-108">All other [*key lengths*](../secgloss/k-gly.md) do not have salt allocated by default.</span></span>

<span data-ttu-id="939fd-109">Sia i provider di base che il provider esteso possono usare il \_ flag crypt No \_ Salt per specificare che non viene allocato alcun valore salt per una chiave simmetrica a 40 bit.</span><span class="sxs-lookup"><span data-stu-id="939fd-109">Both the Base Providers and the Extended Provider can use the CRYPT\_NO\_SALT flag to specify that no salt value is allocated for a 40-bit symmetric key.</span></span> <span data-ttu-id="939fd-110">Le funzioni che accettano questo flag sono [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="939fd-110">The functions that accept this flag are [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey), and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="939fd-111">Per impostazione predefinita, queste funzioni forniscono la compatibilità con le versioni precedenti per la chiave simmetrica a 40 bit continuando l'utilizzo del Salt di valore zero lungo a undici byte.</span><span class="sxs-lookup"><span data-stu-id="939fd-111">By default, these functions provide backward compatibility for the 40-bit symmetric key case by continuing the use of the eleven-byte-long zero-value salt.</span></span>

 

 
