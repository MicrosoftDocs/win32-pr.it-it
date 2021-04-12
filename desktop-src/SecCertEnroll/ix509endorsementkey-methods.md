---
description: L'interfaccia IX509EndorsementKey espone i metodi seguenti.
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: Metodi IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c1eb6a96cd555d4b0a0fdcd2ad52ccf80ec4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233836"
---
# <a name="ix509endorsementkey-methods"></a>Metodi IX509EndorsementKey

L'interfaccia [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) espone i metodi seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                        | Descrizione                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metodo AddCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | Aggiungere un certificato della chiave di verifica dell'autenticità al provider di archiviazione chiavi (KSP) che supporta le chiavi di approvazione.<br/>                                                                                                                                                                                     |
| [**Metodo Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | Chiude la chiave di verifica dell'autenticità. È possibile chiamare il metodo [**Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close) solo dopo che il metodo [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) è stato chiamato correttamente.<br/>                                                                                              |
| [**Metodo ExportPublicKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | Esporta la chiave pubblica di verifica dell'autenticità.<br/>                                                                                                                                                                                                                                                      |
| [**Metodo GetCertificateByIndex**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | Ottiene il certificato di verifica dell'autenticità associato alla chiave di verifica dell'autenticità del provider di archiviazione chiavi per l'indice specificato.<br/>                                                                                                                                                              |
| [**Metodo GetCertificateCount**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | Ottiene il conteggio dei certificati di verifica dell'autenticità nel provider di archiviazione chiavi.<br/>                                                                                                                                                                                                              |
| [**Metodo Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | Apre la chiave di verifica dell'autenticità. È necessario aprire la chiave di verifica dell'autenticità prima di poter recuperare le informazioni dalla chiave di verifica dell'autenticità, aggiungere o rimuovere certificati oppure esportare la chiave di verifica dell'autenticità.<br/>                                                                                                  |
| [**Metodo RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | Rimuove un certificato di verifica dell'autenticità correlato alla chiave di verifica dell'autenticità dal provider di archiviazione chiavi. È possibile chiamare il metodo [**RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate) solo dopo che il metodo [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) è stato chiamato correttamente.<br/> |



 

 

 




