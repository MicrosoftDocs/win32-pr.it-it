---
description: In ognuna delle sezioni seguenti viene illustrata una funzione esportata da Xenroll.dll. In ogni sezione viene inoltre illustrato come utilizzare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Funzioni helper (API di registrazione certificati)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347746"
---
# <a name="helper-functions-certificate-enrollment-api"></a>Funzioni helper (API di registrazione certificati)

In ognuna delle sezioni seguenti viene illustrata una funzione esportata da Xenroll.dll. In ogni sezione viene inoltre illustrato come utilizzare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie.

## <a name="binaryblobtostring"></a>binaryBlobToString

La funzione [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) in Xenroll.dll converte una matrice di byte in una stringa.

Utilizzando CertEnroll.dll, è possibile chiamare il metodo [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) sull'interfaccia [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .

## <a name="stringtobinaryblob"></a>stringToBinaryBlob

La funzione [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) in Xenroll.dll converte una stringa in una matrice di byte.

Utilizzando CertEnroll.dll, è possibile chiamare il metodo [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) sull'interfaccia [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
