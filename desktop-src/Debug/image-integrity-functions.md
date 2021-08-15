---
description: Le funzioni di integrità delle immagini gestiscono il set di certificati in un file di immagine.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Funzioni di integrità delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a2311ccfc59fb228a8f71c380205dc754452ba4a9d0a7e1dcb3c9edcd92a14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957100"
---
# <a name="image-integrity-functions"></a>Funzioni di integrità delle immagini

Le funzioni di integrità delle immagini gestiscono il set di certificati in un file di immagine. Vengono fornite routine per aggiungere, rimuovere ed eseguire query sui certificati. È anche disponibile una funzione per ottenere il flusso di byte di un file di immagine necessario per calcolare un digest del messaggio del file di immagine. Questa operazione è necessaria per creare certificati di firma.

Ogni certificato in un file ha un indice che può cambiare quando i certificati vengono rimossi. I nuovi certificati verranno sempre aggiunti "alla fine" dell'elenco di certificati esistenti. In altre informazioni, verranno assegnati indici maggiori di qualsiasi indice attualmente in uso. In generale, un'applicazione non deve presupporre che un determinato certificato abbia lo stesso indice dell'ultima volta a cui è stato fatto riferimento.

-   [**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



