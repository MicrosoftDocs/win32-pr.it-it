---
description: Le interfacce seguenti possono essere utilizzate per recuperare informazioni sui provider di servizi di crittografia.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Interfacce del provider del crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fa42a9a2704849552fadeb79933d85df9e9f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129887"
---
# <a name="cryptographic-provider-interfaces"></a>Interfacce del provider del crittografia

Le interfacce seguenti possono essere utilizzate per recuperare informazioni sui provider di servizi di crittografia.



| Interfaccia                                    | Descrizione                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | Rappresenta un algoritmo implementato da un provider del crittografia.             |
| [**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | Gestisce una raccolta di oggetti [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) . |
| [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | Consente di accedere alle informazioni generali su un provider di servizi di crittografia.       |
| [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | Gestisce una raccolta di oggetti [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) .  |
| [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | Contiene informazioni su una coppia di provider/algoritmi di crittografia.          |
| [**ICspStatuses**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | Gestisce una raccolta di oggetti [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) .            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



