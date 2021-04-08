---
description: Installa un certificato registrato da un file PFX (Personal Information Exchange) nell'archivio certificati.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968215"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

L'esempio installResponseFromPFX installa un certificato registrato da un file PFX (Personal Information Exchange) nell'archivio certificati.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ installResponseFromPFX

## <a name="discussion"></a>Discussione

Esempio installResponseFromPFX:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere:
    -   Nome dell'esempio.
    -   Nome del file PFX contenente il certificato registrato.
    -   Password associata al file PFX.
2.  Legge il file PFX, provando prima il formato Base64 e il formato binario se Base64 ha esito negativo. La funzione DecodeFileW () è definita in enrollCommon. cpp.
3.  Converte il certificato registrato in un **BSTR** e lo usa per inizializzare un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . La funzione convertWszToBstr è definita in enrollCommon. cpp.
4.  Installa il certificato nell'archivio certificati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[enrollEOBOCMC](enrolleobocmc.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 



