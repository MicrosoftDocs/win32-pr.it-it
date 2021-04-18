---
description: Per creare estensioni personalizzate o per codificare un'estensione complessa, è possibile scrivere gestori di estensioni personalizzati che esportano interfacce personalizzate.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Scrittura di gestori estensioni personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316646"
---
# <a name="writing-custom-extension-handlers"></a>Scrittura di gestori estensioni personalizzati

Per creare estensioni personalizzate o per codificare un'estensione complessa, è possibile scrivere gestori di estensioni personalizzati che esportano interfacce personalizzate. Servizi certificati Microsoft viene fornito con le interfacce seguenti che possono essere usate per codificare diversi tipi di dati di estensione: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)e [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray). Queste interfacce sono contenute in Certenc.dll. Inoltre, le informazioni sul tipo per queste interfacce sono contenute in Certencl.dll, contenuto nella piattaforma Software Development Kit (SDK).

Per altre informazioni sui gestori di estensioni, vedere [gestori di estensioni](extension-handlers.md).

 

 



