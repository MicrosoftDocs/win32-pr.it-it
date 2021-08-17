---
description: Installa un certificato registrato da un file PFX (Personal Information Exchange) nell'archivio certificati.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540e719f098d227afac4af59fd2d296d9d06606d04b9de80cf1e24081918d6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117777607"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

L'esempio installResponseFromPFX installa un certificato registrato da un file PFX (Personal Information Exchange) nell'archivio certificati.

## <a name="location"></a>Località

Quando si installa Microsoft Windows Software Development Kit (SDK), l'esempio viene installato, per impostazione predefinita, nella cartella *%ProgramFiles%* \\ Microsoft SDK Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ installResponseFromPFX .

## <a name="discussion"></a>Discussione

Esempio installResponseFromPFX:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere:
    -   Nome dell'esempio.
    -   Nome del file PFX che contiene il certificato registrato.
    -   Password associata al file PFX.
2.  Legge il file PFX, provando prima il formato base64 e il formato binario se base64 ha esito negativo. La funzione DecodeFileW() è definita in enrollCommon.cpp.
3.  Converte il certificato registrato in **un BSTR e** lo usa per inizializzare un [**oggetto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) La funzione convertWszToBstr è definita in enrollCommon.cpp.
4.  Installa il certificato nell'archivio certificati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[enrollEOBOCMC](enrolleobocmc.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 



