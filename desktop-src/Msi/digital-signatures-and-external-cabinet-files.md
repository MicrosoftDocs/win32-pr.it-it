---
description: Windows Il programma di installazione può usare firme digitali per rilevare le risorse danneggiate.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Firme digitali e file CAB esterni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40edd8527eb93a6b970b3a8ce18fec8cc81f4688804a4e18f7ec5cdd748f3eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947465"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>Firme digitali e file CAB esterni

Windows Il programma di installazione può usare firme digitali per rilevare le risorse danneggiate. Quando si installa una risorsa esterna, il certificato del firmatario appartenente alla risorsa può essere verificato rispetto a un certificato firmatario di riferimento creato nel pacchetto. Il programma di installazione non è in grado di verificare le firme per i file cab interni. Può verificare solo le firme digitali usando la [tabella MsiDigitalSignature](msidigitalsignature-table.md) e [la tabella MsiDigitalCertificate](msidigitalcertificate-table.md).

Windows Il programma di installazione esegue le operazioni seguenti quando si installa un file archiviato in un archivio esterno:

-   Il programma di installazione verifica se la voce del supporto per l'archivio esterno è elencata nella [tabella MsiDigitalSignature](msidigitalsignature-table.md). Un file archiviato in un archivio esterno viene identificato dalla presenza di una voce nella colonna Cabinet della tabella [Media](media-table.md) non preceduta da un carattere \# ''.
-   Prima di aprire l'archivio esterno, il programma di installazione chiama WinVerifyTrust per estrarre il certificato corrente e le informazioni hash. In caso di mancata corrispondenza tra le informazioni sulla firma correnti nell'archivio e le informazioni sulla firma scritte nel pacchetto, l'installazione non riesce. L'installazione non riesce perché l'archivio potrebbe essere stato compromesso e non può essere considerato attendibile.

Per altre informazioni sull'uso di firme digitali, certificati digitali e [](https://msdn.microsoft.com/library/cc527452.aspx) [**WinVerifyTrust,**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)vedere la sezione Sicurezza di Microsoft Windows Software Development Kit (SDK).

Per altre informazioni, vedere [**MsiGetFileSignatureInformation,**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa) [la tabella MsiDigitalCertificate](msidigitalcertificate-table.md)e [la tabella MsiDigitalSignature](msidigitalsignature-table.md).

 

 
