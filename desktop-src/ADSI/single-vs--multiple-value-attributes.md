---
title: Attributi a valore singolo e multiplo
description: Gli attributi che possono esistere in una directory sono in genere definiti nello schema per la directory.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- attributi a valore singolo o multiplo ADSI
- attributi ADSI, attributi a valore singolo o multiplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd9442a5365efbe343c2a9af74aa8576928e7a6a383cc131a3384152c2b1c0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262031"
---
# <a name="single-vs-multiple-value-attributes"></a>Attributi a valore singolo e multiplo

Gli attributi che possono esistere in una directory sono in genere definiti nello schema per la directory. La definizione dello schema di un attributo specifica una serie di caratteristiche dell'attributo, ad esempio il tipo di dati e se un'istanza dell'attributo può avere più valori.

Un'istanza di un attributo a valore singolo può contenere un singolo valore. Un'istanza di un attributo multivalore può contenere un singolo valore o più valori. Active Directory non crea attributi con valori vuoti: l'attributo contiene un valore valido o non esiste nell'oggetto.

> [!Note]  
> In Active Directory e nella maggior parte degli altri server LDAP, l'ordine dei valori in un attributo multivalore non è definito. Inoltre, ogni valore di un attributo multivalore deve essere univoco.

 

ADSI carica in genere i dati dello schema se la directory supporta uno schema, come active directory. Poiché ADSI conosce la sintassi degli attributi nello schema, non è necessario specificare il tipo di attributo quando vi si accede. ADSI effettua il marshalling dei valori degli attributi nel tipo di dati appropriato, come definito nello schema.

Se la directory non ha uno schema, specificare il tipo di dati quando si accede a un attributo.

> [!Note]  
> Active Directory, Exchange, Windows NT 4.0 e Site Server hanno tutti uno schema. Active Directory dispone inoltre di uno schema estendibile.

 

 

 




