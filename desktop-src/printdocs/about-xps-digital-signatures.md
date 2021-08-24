---
description: Questa sezione offre una panoramica dell'API di firma digitale XPS.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: Informazioni sull'API di firma digitale XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcfbd6000df56d96afbc86a3cd0111c02a128c3c23c0d0de59717da5f4e9ac6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950941"
---
# <a name="about-xps-digital-signature-api"></a>Informazioni sull'API di firma digitale XPS

I documenti XPS possono avere firme digitali per consentire agli utenti di firmare un documento, verificare l'identità del firmatario e indicare se un documento XPS è stato modificato dopo la firma. Un'Windows nativa può usare le interfacce dell'API di firma digitale XPS per eseguire operazioni di firma digitale su un documento XPS. Questa sezione offre una panoramica dell'API di firma digitale XPS.

[**L'interfaccia IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) gestisce le operazioni di firma digitale in un documento XPS. Prima che un'applicazione possa accedere alle firme digitali di un documento XPS, l'applicazione deve chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un **oggetto IXpsSignatureManager** e quindi [**chiamare IXpsSignatureManager::LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) o [**IXpsSignatureManager::LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) per caricare il documento XPS. Per altre informazioni su questo processo di inizializzazione, vedere [Inizializzare il gestore delle firme.](initialize-the-signature-manager.md)

Dopo che un documento XPS è stato caricato in [**un'interfaccia IXpsSignatureManager,**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) un'applicazione può accedere alle firme digitali e alle richieste di firma digitale del documento. È possibile accedere alle firme digitali usando [**un'interfaccia IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) dall'interfaccia [**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) del gestore delle firme. Un'applicazione può anche aggiungere e rimuovere **interfacce IXpsSignature** dalla raccolta. Le richieste di firma sono accessibili [**tramite IXpsSignatureRequest,**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) raccolte in [**un'interfaccia IXpsSignatureRequestCollection.**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) **IXpsSignatureRequestCollection** fa parte di [**un'interfaccia IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) raccolta in [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) del gestore delle firme.

Le applicazioni possono usare [**IXpsSigningOptions del**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) gestore delle firme per accedere alle opzioni di firma digitale e impostarne le opzioni.

Per esempi su come accedere alle firme digitali di un documento XPS, vedere [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di firma digitale XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Informazioni di riferimento sulle API di firma digitale XPS](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Standard ECMA-376, Office di file Open XML](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
