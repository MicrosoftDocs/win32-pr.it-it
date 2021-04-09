---
title: Attributi singolo e più valori
description: Gli attributi che possono esistere in una directory sono in genere definiti nello schema per la directory.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- ADSI singolo e più attributi di valore
- attributi ADSI, Single rispetto a più attributi di valore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044051"
---
# <a name="single-vs-multiple-value-attributes"></a>Attributi singolo e più valori

Gli attributi che possono esistere in una directory sono in genere definiti nello schema per la directory. La definizione dello schema di un attributo specifica un numero di caratteristiche dell'attributo, ad esempio il tipo di dati e se un'istanza dell'attributo può avere più valori.

Un'istanza di un attributo a valore singolo può contenere un solo valore. Un'istanza di un attributo multivalore può contenere un solo valore o più valori. Active Directory non crea attributi con valori vuoti, l'attributo contiene un valore valido o non esiste nell'oggetto.

> [!Note]  
> In Active Directory e nella maggior parte degli altri server LDAP, l'ordine dei valori in un attributo multivalore non è definito. Inoltre, ogni valore di un attributo multivalore deve essere univoco.

 

In genere, ADSI carica i dati dello schema se la directory supporta uno schema, come Active Directory. Poiché ADSI conosce la sintassi degli attributi nello schema, non è necessario specificare il tipo di attributo durante l'accesso. ADSI esegue il marshalling dei valori di attributo nel tipo di dati appropriato come definito nello schema.

Se la directory non dispone di alcuno schema, specificare il tipo di dati per l'accesso a un attributo.

> [!Note]  
> Active Directory, Exchange, Windows NT 4,0 e il server del sito hanno tutti uno schema. Inoltre, Active Directory dispone di uno schema estendibile.

 

 

 




