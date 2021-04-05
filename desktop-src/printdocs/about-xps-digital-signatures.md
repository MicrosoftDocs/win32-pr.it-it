---
description: Questa sezione fornisce una panoramica dell'API di firma digitale XPS.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: Informazioni sull'API di firma digitale XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba2bad4ef10d8800e9a4cb59289fccb75cc2d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131602"
---
# <a name="about-xps-digital-signature-api"></a>Informazioni sull'API di firma digitale XPS

I documenti XPS possono avere firme digitali per consentire agli utenti di firmare un documento, verificare l'identità del firmatario e indicare se un documento XPS è stato modificato dopo la firma. Un'applicazione Windows nativa può utilizzare le interfacce dell'API XPS Digital Signature per eseguire operazioni di firma digitale in un documento XPS. Questa sezione fornisce una panoramica dell'API di firma digitale XPS.

L'interfaccia [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) gestisce le operazioni di firma digitale in un documento XPS. Prima che un'applicazione possa accedere alle firme digitali di un documento XPS, l'applicazione deve chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un **IXpsSignatureManager** e quindi chiamare [**IXpsSignatureManager:: LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) o [**IXpsSignatureManager:: LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) per caricare il documento XPS. Per ulteriori informazioni su questo processo di inizializzazione, vedere [Initialize the Signature Manager](initialize-the-signature-manager.md).

Dopo che un documento XPS è stato caricato in un'interfaccia [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) , un'applicazione può quindi accedere alle firme digitali e alle richieste di firma digitale del documento. È possibile accedere alle firme digitali usando un'interfaccia [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) dall'interfaccia [**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) di gestione della firma. Un'applicazione può anche aggiungere e rimuovere le interfacce **IXpsSignature** dalla raccolta. È possibile accedere alle richieste di firma usando [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) raccolte in un'interfaccia [**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) . **IXpsSignatureRequestCollection** fa parte di un'interfaccia [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) che vengono raccolti nel [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) di gestione della firma.

Le applicazioni possono utilizzare [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) di gestione firme per accedere e impostare le opzioni di firma digitale.

Per esempi relativi all'accesso alle firme digitali di un documento XPS, vedere [attività comuni di programmazione della firma digitale](basic-digital-signature-programming-tasks.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di firma digitale XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Informazioni di riferimento sull'API di firma digitale XPS](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Standard ECMA-376, formati di file Office Open XML](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
