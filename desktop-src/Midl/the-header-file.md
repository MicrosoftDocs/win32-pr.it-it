---
title: Il file di intestazione
description: Il file di intestazione contiene le definizioni di tutti i tipi di dati e le operazioni dichiarate nel file IDL, nonché tutti i tipi di dati e le operazioni dichiarati nei file inclusi con la direttiva \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL e RPC MIDL, interfacce, file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045049"
---
# <a name="the-header-file"></a>Il file di intestazione

Il file di intestazione contiene le definizioni di tutti i tipi di dati e le operazioni dichiarate nel file IDL, nonché tutti i tipi di dati e le operazioni dichiarati nei file inclusi con la \# direttiva include. I tipi di dati dei file importati con la direttiva Import non vengono replicati nel file di intestazione. il file di intestazione generato contiene invece una riga di inclusione per il file H generato dal file importato. Il file di intestazione deve essere incluso in tutti i moduli dell'applicazione che chiamano le operazioni definite, implementano le operazioni definite o modificano i tipi definiti.

Il compilatore MIDL passa [**/header**](-header.md) e [**/out**](-out.md) influisce sul file di intestazione.

 

 




