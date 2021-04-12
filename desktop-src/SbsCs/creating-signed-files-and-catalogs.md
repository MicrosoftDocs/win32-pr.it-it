---
description: Per firmare un file e creare un catalogo, è necessario innanzitutto disporre di un processo per la firma di file, un certificato e una chiave pubblica.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Creazione di file e cataloghi firmati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231848"
---
# <a name="creating-signed-files-and-catalogs"></a>Creazione di file e cataloghi firmati

Per firmare un file e creare un catalogo, è necessario innanzitutto disporre di un processo per la firma di file, un certificato e una chiave pubblica.

**Per firmare un file e creare un catalogo**

1.  Usare [Pktextract.exe](pktextract-exe.md) per estrarre il [*token di chiave pubblica*](p-sbscs-gly.md) dal file del certificato. Il file del certificato deve essere presente nella stessa directory dell'utilità.
2.  Usare il valore del token di chiave pubblica per aggiornare l'attributo **PublicKeyToken** dell'elemento **assemblyIdentity** nel file manifesto.
3.  Usare [MT.exe](mt-exe.md) per generare hash di file contenuti nel manifesto dell'assembly e per creare il file di descrizione del catalogo (. CDF).
4.  Utilizzare Makecat.exe con il. CDF generato per creare il catalogo di sicurezza per l'assembly. Questo strumento è incluso in CryptoAPI.
5.  Usare l'utilità [SignTool](/windows/desktop/SecCrypto/signtool) per firmare il catalogo generato con il certificato usato nel passaggio 1. Il. CDF dei passaggi 3 e 4 può essere eliminato una volta creato il catalogo.

Vedere anche [esempio di firma degli assembly](assembly-signing-example.md).

 

 
