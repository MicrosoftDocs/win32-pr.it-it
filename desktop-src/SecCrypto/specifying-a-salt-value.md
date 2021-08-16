---
description: Sia il provider di base che il provider esteso possono specificare il valore e la lunghezza del valore salt da utilizzare. Il provider di base imposta un valore salt usando il valore del parametro \_ KP SALT. Il provider di base imposta sempre 11 byte di valore salt.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Specifica di un valore Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d80ca64bc69cbcf0ed98d72b5b061616fc3cf641f3970d1533b094ef5687f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897946"
---
# <a name="specifying-a-salt-value"></a>Specifica di un valore Salt

Sia il provider di base che il provider esteso possono specificare il valore e la lunghezza del valore [*salt*](../secgloss/s-gly.md) da utilizzare. Il provider di base imposta un valore salt usando il valore del parametro \_ KP SALT. Il provider di base imposta sempre 11 byte di valore salt.

Il provider avanzato imposta il valore salt chiamando [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con il valore del parametro KP SALT EX specificato e con il \_ \_ parametro *pbData* che punta a una struttura [**BLOB CRYPT \_ INTEGER \_**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) che contiene il salt.

> [!Note]  
> La lunghezza totale di una chiave simmetrica del [*provider*](../secgloss/s-gly.md) avanzato e del relativo valore salt non può essere maggiore di 128 bit.

 

KP \_ SALT continua a essere fornito per garantire la compatibilità con le versioni precedenti con il provider di base. Le applicazioni più nuove devono usare il valore del parametro \_ KP SALT \_ EX.

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



 

 
