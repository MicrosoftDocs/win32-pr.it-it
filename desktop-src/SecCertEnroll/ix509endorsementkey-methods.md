---
description: L'interfaccia IX509EndorsementKey espone i metodi seguenti.
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: Metodi IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83bc951830f308e2918558794c9790c9f57183ca250e17b7821ba2a152428576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881731"
---
# <a name="ix509endorsementkey-methods"></a>Metodi IX509EndorsementKey

[**L'interfaccia IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) espone i metodi seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                        | Descrizione                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metodo AddCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | Aggiungere un certificato della chiave di verifica dell'approvazione al provider di archiviazione chiavi (KSP) che supporta le chiavi di verifica dell'approvazione.<br/>                                                                                                                                                                                     |
| [**Metodo Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | Chiude la chiave di approvazione. È possibile chiamare il [**metodo Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close) solo dopo che il [**metodo Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) è stato chiamato correttamente.<br/>                                                                                              |
| [**Metodo ExportPublicKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | Esporta la chiave pubblica di approvazione.<br/>                                                                                                                                                                                                                                                      |
| [**Metodo GetCertificateByIndex**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | Ottiene il certificato di approvazione associato alla chiave di approvazione dal provider di archiviazione chiavi per l'indice specificato.<br/>                                                                                                                                                              |
| [**Metodo GetCertificateCount**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | Ottiene il conteggio dei certificati di approvazione nel provider di archiviazione chiavi.<br/>                                                                                                                                                                                                              |
| [**Metodo Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | Apre la chiave di approvazione. La chiave di verifica dell'approvazione deve essere aperta prima di poter recuperare informazioni dalla chiave di verifica dell'approvazione, aggiungere o rimuovere certificati o esportare la chiave di verifica dell'approvazione.<br/>                                                                                                  |
| [**Metodo RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | Rimuove un certificato di verifica dell'approvazione correlato alla chiave di verifica dell'approvazione dal provider di archiviazione chiavi. È possibile chiamare il [**metodo RemoveCertificate solo**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate) dopo che il [**metodo Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) è stato chiamato correttamente.<br/> |



 

 

 




