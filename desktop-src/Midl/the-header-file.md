---
title: File di intestazione
description: Il file di intestazione contiene le definizioni di tutti i tipi di dati e di tutte le operazioni dichiarate nel file IDL, nonché di tutti i tipi di dati e le operazioni dichiarati nei file inclusi nella direttiva \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL e RPC MIDL , interfacce, file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd107bbf741f3259ac474d03a3ec1eba5c4ab8217df3ff6afa5ef45e7b4945a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582131"
---
# <a name="the-header-file"></a>File di intestazione

Il file di intestazione contiene le definizioni di tutti i tipi di dati e di tutte le operazioni dichiarate nel file IDL, nonché di tutti i tipi di dati e le operazioni dichiarati nei file inclusi nella \# direttiva include. I tipi di dati dei file importati con la direttiva import non vengono replicati nel file di intestazione. il file di intestazione generato contiene invece una riga di inclusione per il file H generato dal file importato. Il file di intestazione deve essere incluso da tutti i moduli dell'applicazione che chiamano le operazioni definite, implementano le operazioni definite o modificano i tipi definiti.

Le opzioni /header e [**/out**](-out.md) del [**compilatore**](-header.md) MIDL influiscono sul file di intestazione.

 

 




