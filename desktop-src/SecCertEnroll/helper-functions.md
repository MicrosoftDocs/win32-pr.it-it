---
description: Ognuna delle sezioni seguenti illustra una funzione esportata da Xenroll.dll. Ogni sezione illustra anche come usare CertEnroll.dll per sostituire la funzione o indica che non esiste alcun mapping tra le due librerie.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Funzioni helper (API di registrazione certificati)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c99282099f93482e3064a00eed146464a8d537e70d803b3b51389f92d9f93912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119669831"
---
# <a name="helper-functions-certificate-enrollment-api"></a>Funzioni helper (API di registrazione certificati)

Ognuna delle sezioni seguenti illustra una funzione esportata da Xenroll.dll. Ogni sezione illustra anche come usare CertEnroll.dll per sostituire la funzione o indica che non esiste alcun mapping tra le due librerie.

## <a name="binaryblobtostring"></a>binaryBlobToString

La [**funzione binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) in Xenroll.dll converte una matrice di byte in una stringa.

Usando CertEnroll.dll, è possibile chiamare il [**metodo VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) sull'interfaccia [**IBinaryConverter.**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)

## <a name="stringtobinaryblob"></a>stringToBinaryBlob

La [**funzione stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) in Xenroll.dll converte una stringa in una matrice di byte.

Usando CertEnroll.dll, è possibile chiamare il [**metodo StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) sull'interfaccia [**IBinaryConverter.**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
