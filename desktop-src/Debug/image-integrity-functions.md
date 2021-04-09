---
description: Le funzioni di integrità dell'immagine gestiscono il set di certificati in un file di immagine.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Funzioni di integrità immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049166"
---
# <a name="image-integrity-functions"></a>Funzioni di integrità immagini

Le funzioni di integrità dell'immagine gestiscono il set di certificati in un file di immagine. Vengono fornite routine per aggiungere, rimuovere ed eseguire query sui certificati. È disponibile anche una funzione per ottenere il flusso di byte di un file di immagine necessario per calcolare un digest del messaggio del file di immagine. Questa operazione è necessaria per creare certificati di firma.

Ogni certificato in un file dispone di un indice che può essere modificato quando vengono rimossi i certificati. I nuovi certificati verranno sempre aggiunti "alla fine" dell'elenco dei certificati esistenti. Ovvero verranno assegnati indici che sono maggiori di tutti gli indici attualmente in uso. In generale, un'applicazione non deve presupporre che un determinato certificato abbia lo stesso indice con l'ultima volta in cui è stato fatto riferimento.

-   [**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



