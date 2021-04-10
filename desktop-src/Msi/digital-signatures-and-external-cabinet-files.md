---
description: Windows Installer possibile utilizzare le firme digitali per rilevare le risorse danneggiate.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Firme digitali e file CAB esterni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10e921b324a43a919a417f47953c0a44e4777ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882982"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>Firme digitali e file CAB esterni

Windows Installer possibile utilizzare le firme digitali per rilevare le risorse danneggiate. Quando si installa una risorsa esterna, il certificato del firmatario appartenente alla risorsa può essere verificato rispetto a un certificato del firmatario di riferimento creato nel pacchetto. Il programma di installazione non è in grado di verificare le firme per i cabinet interni. Può verificare solo le firme digitali usando la [tabella MsiDigitalSignature](msidigitalsignature-table.md) e la [tabella MsiDigitalCertificate](msidigitalcertificate-table.md).

Quando si installa un file archiviato in un file CAB esterno, Windows Installer esegue le operazioni seguenti:

-   Il programma di installazione verifica se la voce relativa ai supporti per il cabinet esterno è elencata nella [tabella MsiDigitalSignature](msidigitalsignature-table.md). Un file archiviato in un file CAB esterno viene identificato con una voce nella colonna CAB della [tabella multimediale](media-table.md) che non è preceduta da un \# carattere ''.
-   Prima di aprire il file CAB esterno, il programma di installazione chiama WinVerifyTrust per estrarre il certificato e le informazioni hash correnti. In caso di mancata corrispondenza tra le informazioni sulla firma corrente nel file CAB e le informazioni sulla firma create nel pacchetto, l'installazione non riesce. L'installazione non riesce perché il cabinet potrebbe essere stato compromesso e non può essere considerato attendibile.

Per ulteriori informazioni sull'utilizzo di firme digitali, certificati digitali e [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), vedere la sezione relativa alla [sicurezza](https://msdn.microsoft.com/library/cc527452.aspx) di Microsoft Windows Software Development Kit (SDK).

Per ulteriori informazioni, vedere [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [tabella MsiDigitalCertificate](msidigitalcertificate-table.md)e [tabella MsiDigitalSignature](msidigitalsignature-table.md).

 

 
