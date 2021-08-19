---
description: Di seguito sono riportate le funzioni ImageHlp.
ms.assetid: 926f412e-25ba-4f9c-a118-b5a1bc723379
title: Funzioni imageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2650d80dfb78f346a5fab22e0adfabdfb11c8e626ad3b5ea39930337feaebe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957110"
---
# <a name="imagehlp-functions"></a>Funzioni imageHlp

Di seguito sono riportate le funzioni ImageHlp.

## <a name="image-access"></a>Accesso alle immagini

Le funzioni di accesso alle immagini accedono ai dati in un'immagine eseguibile. Le funzioni forniscono un accesso di alto livello alla base delle immagini e un accesso molto specifico alle parti più comuni dei dati di un'immagine.

<dl>

[**GetImageConfigInformation**](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageconfiginformation)  
[**GetImageUnusedHeaderBytes**](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageunusedheaderbytes)  
[**ImageLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageload)  
[**ImageUnload**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageunload)  
[**MapAndLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-mapandload)  
[**SetImageConfigInformation**](/windows/desktop/api/Imagehlp/nf-imagehlp-setimageconfiginformation)  
[**UnMapAndLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-unmapandload)  
</dl>

## <a name="image-integrity"></a>Integrità delle immagini

Le funzioni di integrità delle immagini gestiscono il set di certificati in un file di immagine.

<dl>

[**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)  
[**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)  
[**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)  
[**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)  
[**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)  
[**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)  
[**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)  
</dl>

## <a name="image-modification"></a>Modifica dell'immagine

Le funzioni di modifica dell'immagine consentono di modificare l'immagine eseguibile.

<dl>

[**BindImage**](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)  
[**BindImageEx**](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)  
[**CheckSumMappedFile**](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)  
[**MapFileAndCheckSum**](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)  
[**ReBaseImage**](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)  
[**ReBaseImage64**](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage64)  
[**SplitSymbols**](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)  
[**StatusRoutine**](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)  
[**TouchFileTimes**](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)  
[**UpdateDebugInfoFile**](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)  
[**UpdateDebugInfoFileEx**](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)  
</dl>

 

 



