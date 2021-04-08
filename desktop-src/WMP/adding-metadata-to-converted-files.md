---
title: Aggiunta di metadati ai file convertiti
description: Aggiunta di metadati ai file convertiti
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Media Player Windows, processo di conversione
- Plug-in di Windows Media Player, conversione
- plug-in, conversione
- plug-in di conversione, aggiunta di metadati ai file convertiti
- Aggiunta di metadati ai file convertiti
- metadati, aggiunta ai file convertiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727735"
---
# <a name="adding-metadata-to-converted-files"></a>Aggiunta di metadati ai file convertiti

I file convertiti devono contenere determinati metadati per garantire un'esperienza utente ottimale. Come minimo, i file convertiti devono contenere gli attributi primari elencati nelle [linee guida sull'utilizzo dei metadati di Windows Media](/previous-versions/ms867702(v=msdn.10)).

Per file musicali, impostare il valore per **WM/MediaClassPrimaryID** su D1607DBC-E323-4BE2-86A1-48A42A28441E.

Per i file della segreteria telefonica, impostare il valore per **WM/MediaClassPrimaryID** su 01CD0F29-DA4E-4157-897b-6275D50C4F11, ovvero il GUID della classe primaria per i file audio. Impostare il valore per **WM/MediaClassSecondaryID** su 193c8824-4D52-4178-90bd-305240b04636.

Per le note vocali, impostare il valore per **WM/MediaClassPrimaryID** su 01CD0F29-DA4E-4157-897b-6275D50C4F11. Impostare il valore per **WM/MediaClassSecondaryID** su 3A172A13-2BD9-4831-835B-114F6A95943F.

Impostare il valore per **WM/contentdistributor** sul nome della chiave per il servizio Music che ha fornito il contenuto.

Impostare il valore per **WM/UniqueFileIdentifier** sull'ID contenuto. Ciò consentirà di recuperare elementi di contenuto specifici in un momento successivo.

Impostare un valore per **WM/WMShadowFileSourceFileType**.

Per il contenuto protetto, usare Windows Media Format SDK per impostare l'attributo **DRM \_ DRMHeader \_ ContentID** sull'ID contenuto.

Per contenuto protetto, impostare un valore per **WM/WMShadowFileSourceDRMType**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui plug-in di conversione**](about-conversion-plug-ins.md)
</dt> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 