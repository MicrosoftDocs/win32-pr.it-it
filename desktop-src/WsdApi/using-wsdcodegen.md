---
description: Descrive il processo di compilazione di un'applicazione WSDAPI usando WsdCodeGen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Uso di WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e09bd2b0c8f96d51751aa90bc3206a0824f19b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312672"
---
# <a name="using-wsdcodegen"></a>Uso di WsdCodeGen

**Per compilare un'applicazione WSDAPI usando WsdCodeGen**

1.  Definire il contratto funzionale per l'host del dispositivo in un file WSDL.
2.  Generare un file di configurazione usando WsdCodeGen. Per altre informazioni, vedere [file di configurazione di WsdCodeGen](wsdcodegen-configuration-file.md) e [sintassi della riga di comando di WsdCodeGen](wsdcodegen-command-line-syntax.md).
3.  Aprire il file di configurazione generato e modificare il file in modo che sia necessario. Se si sta compilando un'applicazione client, è necessaria una modifica minima o nulla. Se si compila un'applicazione host, modificare gli elementi di configurazione specifici dell'utente, ad esempio [**Manufacturer**](manufacturer.md) e [**ModelName**](modelname.md).
4.  Generare il codice usando WsdCodeGen, specificando il file di configurazione come input. Per ulteriori informazioni, vedere [sintassi della riga di comando WsdCodeGen](wsdcodegen-command-line-syntax.md).
5.  Usare il codice generato per compilare un client, un host o entrambi.

Il Windows SDK include alcuni file WSDL di esempio, i file di configurazione WsdCodeGen e il codice generato. Per ulteriori informazioni, vedere [WSDAPI Samples](wsdapi-samples.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 



