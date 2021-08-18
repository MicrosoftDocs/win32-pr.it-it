---
description: Per firmare un file e creare un catalogo per esso, è innanzitutto necessario disporre di un processo per la firma di file, un certificato e una chiave pubblica.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Creazione di file e cataloghi firmati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9abcccc2451cfa9461bc8129705c1094291b33fea609679c89ef46d7cf7348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142324"
---
# <a name="creating-signed-files-and-catalogs"></a>Creazione di file e cataloghi firmati

Per firmare un file e creare un catalogo per esso, è innanzitutto necessario disporre di un processo per la firma di file, un certificato e una chiave pubblica.

**Per firmare un file e creare un catalogo**

1.  Usare [Pktextract.exe](pktextract-exe.md) per estrarre il [*token di chiave*](p-sbscs-gly.md) pubblica dal file del certificato. Il file del certificato deve essere presente nella stessa directory dell'utilità .
2.  Usare il valore del token di chiave pubblica per aggiornare **l'attributo publicKeyToken** **dell'elemento assemblyIdentity** nel file manifesto.
3.  Usare [MT.exe](mt-exe.md) per generare hash dei file contenuti nel manifesto dell'assembly e per creare il file di descrizione del catalogo (con estensione cdf).
4.  Usare Makecat.exe con il file CDF generato per creare il catalogo di sicurezza per l'assembly. Questo strumento è incluso in CryptoAPI.
5.  Usare [l'utilità SignTool](/windows/desktop/SecCrypto/signtool) per firmare il catalogo generato con il certificato usato nel passaggio 1. Il file con estensione cdf dei passaggi 3 e 4 può essere eliminato dopo la creazione del catalogo.

Vedere anche Esempio [di firma degli assembly.](assembly-signing-example.md)

 

 
