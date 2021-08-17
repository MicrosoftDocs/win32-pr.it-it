---
description: Le interfacce seguenti possono essere utilizzate per recuperare informazioni sui provider del servizio di crittografia.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Interfacce del provider del servizio di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e39e42f17efdeae353b02723522e744031a394e8faa8a4be986831087561e4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976911"
---
# <a name="cryptographic-provider-interfaces"></a>Interfacce del provider del servizio di crittografia

Le interfacce seguenti possono essere utilizzate per recuperare informazioni sui provider del servizio di crittografia.



| Interfaccia                                    | Descrizione                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | Rappresenta un algoritmo implementato da un provider del servizio di crittografia.             |
| [**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | Gestisce una raccolta di [**oggetti ICspAlgorithm.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) |
| [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | Fornisce l'accesso alle informazioni generali su un provider del servizio di crittografia.       |
| [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | Gestisce una raccolta di [**oggetti ICspInformation.**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)  |
| [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | Contiene informazioni su una coppia provider/algoritmo di crittografia.          |
| [**ICspStatuses**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | Gestisce una raccolta di [**oggetti ICspStatus.**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



