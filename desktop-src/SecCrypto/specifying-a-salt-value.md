---
description: Sia il provider di base che il provider esteso possono specificare il valore e la lunghezza del valore salt da usare. Il provider di base imposta un valore salt usando il \_ valore del parametro Salt di KP. Il provider di base imposta sempre undici byte di valore salt.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Specifica di un valore Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc8aeea66c536db1c24d7ef3cf4fb9a05b543f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319346"
---
# <a name="specifying-a-salt-value"></a><span data-ttu-id="a992a-105">Specifica di un valore Salt</span><span class="sxs-lookup"><span data-stu-id="a992a-105">Specifying a Salt Value</span></span>

<span data-ttu-id="a992a-106">Sia il provider di base che il provider esteso possono specificare il valore e la lunghezza del [*valore salt*](../secgloss/s-gly.md) da usare.</span><span class="sxs-lookup"><span data-stu-id="a992a-106">Both the Base Provider and the Extended Provider can specify the value and length of the [*salt value*](../secgloss/s-gly.md) to be used.</span></span> <span data-ttu-id="a992a-107">Il provider di base imposta un valore salt usando il \_ valore del parametro Salt di KP.</span><span class="sxs-lookup"><span data-stu-id="a992a-107">The Base Provider sets a salt value using the KP\_SALT parameter value.</span></span> <span data-ttu-id="a992a-108">Il provider di base imposta sempre undici byte di valore salt.</span><span class="sxs-lookup"><span data-stu-id="a992a-108">The Base Provider always sets eleven bytes of salt value.</span></span>

<span data-ttu-id="a992a-109">Il provider migliorato imposta il valore salt chiamando [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con il valore del \_ parametro PK Salt \_ ex specificato e con il parametro *pbData* che punta a una struttura [**\_ \_ BLOB Integer Crypt**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) che contiene il Salt.</span><span class="sxs-lookup"><span data-stu-id="a992a-109">The Enhanced Provider sets the salt value by calling [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) with the KP\_SALT\_EX parameter value specified and with the *pbData* parameter pointing to a [**CRYPT\_INTEGER\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains the salt.</span></span>

> [!Note]  
> <span data-ttu-id="a992a-110">La lunghezza totale di una [*chiave simmetrica*](../secgloss/s-gly.md) del provider avanzata e del relativo valore salt non può essere maggiore di 128 bit.</span><span class="sxs-lookup"><span data-stu-id="a992a-110">The total length of an Enhanced Provider [*symmetric key*](../secgloss/s-gly.md) and its salt value cannot be greater than 128 bits.</span></span>

 

<span data-ttu-id="a992a-111">\_Il Salt KP continua a essere fornito per la compatibilità con le versioni precedenti del provider di base.</span><span class="sxs-lookup"><span data-stu-id="a992a-111">KP\_SALT continues to be provided for backward compatibility with the Base Provider.</span></span> <span data-ttu-id="a992a-112">Le applicazioni più recenti devono usare il \_ valore del parametro PK Salt \_ es.</span><span class="sxs-lookup"><span data-stu-id="a992a-112">Newer applications should use the KP\_SALT\_EX parameter value.</span></span>

<span data-ttu-id="a992a-113">Nell'esempio seguente viene impostato un valore salt.</span><span class="sxs-lookup"><span data-stu-id="a992a-113">The following example sets a salt value.</span></span>


```C++
// Specify 4 bytes of salt.
BYTE rgbSalt[] = {0x01, 0x02, 0x03, 0x04};
CRYPT_DATA_BLOB sSaltData;
sSaltData.pbData = rgbSalt;
sSaltData.cbData = sizeof(rgbSalt);

// Set the 4 bytes of salt required.
// hKey is an HCRYPTPROV handle previously
// assigned, such as by CryptImportKey.
if (CryptSetKeyParam(
        hKey,    
        KP_SALT_EX,    
        (BYTE*)&sSaltData,    
        0))
{
     printf("The salt value is set.\n");
}
else
{
     printf("Setting the salt value failed.\n");
}
```



 

 
