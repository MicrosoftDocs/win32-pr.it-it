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
# <a name="specifying-a-salt-value"></a>Specifica di un valore Salt

Sia il provider di base che il provider esteso possono specificare il valore e la lunghezza del [*valore salt*](../secgloss/s-gly.md) da usare. Il provider di base imposta un valore salt usando il \_ valore del parametro Salt di KP. Il provider di base imposta sempre undici byte di valore salt.

Il provider migliorato imposta il valore salt chiamando [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con il valore del \_ parametro PK Salt \_ ex specificato e con il parametro *pbData* che punta a una struttura [**\_ \_ BLOB Integer Crypt**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) che contiene il Salt.

> [!Note]  
> La lunghezza totale di una [*chiave simmetrica*](../secgloss/s-gly.md) del provider avanzata e del relativo valore salt non può essere maggiore di 128 bit.

 

\_Il Salt KP continua a essere fornito per la compatibilità con le versioni precedenti del provider di base. Le applicazioni più recenti devono usare il \_ valore del parametro PK Salt \_ es.

Nell'esempio seguente viene impostato un valore salt.


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



 

 
