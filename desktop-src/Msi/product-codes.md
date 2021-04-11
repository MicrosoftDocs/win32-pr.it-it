---
description: Il codice del prodotto è un GUID che rappresenta l'identificazione principale di un'applicazione o di un prodotto.
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: Codici prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edca03d54dcd14068e89b2314b729e672b0c631c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232972"
---
# <a name="product-codes"></a>Codici prodotto

Il codice del prodotto è un GUID che rappresenta l'identificazione principale di un'applicazione o di un prodotto. Per ulteriori informazioni, vedere la proprietà [**ProductCode**](productcode.md) . Se vengono apportate modifiche significative a un prodotto, anche il codice del prodotto deve essere modificato in modo da riflettere questo problema. Non è tuttavia necessario che il codice del prodotto venga modificato se le modifiche apportate al prodotto sono relativamente minori.

Le versioni a 32 e 64 bit del pacchetto di un'applicazione devono avere codici prodotto diversi. Se un componente a 32 bit di un'applicazione viene ricompilato in un componente a 64 bit, è necessario assegnare un nuovo codice del prodotto.

Se un server esposto nella [tabella PublishComponent](publishcomponent-table.md) viene ricompilato da 32 bit a 64 bit, potrebbe essere necessario modificare anche il GUID in questa tabella in modo che i client a 32 bit e a 64 bit possano identificare la categoria di componenti qualificati appropriata. In questo caso, è necessario modificare anche il codice prodotto.

Si noti che le lettere nei GUID del codice prodotto devono essere maiuscole. Utilità come GUIDGEN generano GUID contenenti lettere minuscole. Le lettere minuscole in questi GUID devono essere modificate in lettere maiuscole per essere utilizzate come codice del prodotto o codice del pacchetto. Per ulteriori informazioni, vedere [modifica del codice del prodotto](changing-the-product-code.md).

Il codice del pacchetto è un GUID che identifica un particolare [*pacchetto*](p-gly.md)di Windows Installer. Il codice del pacchetto associa un file con estensione msi a un'applicazione o a un prodotto e può essere usato anche per la verifica delle origini. I codici prodotto e pacchetto non sono intercambiabili. Due file con estensione msi non identici dovrebbero avere sempre lo stesso codice del pacchetto. Sebbene sia comune spedire un'applicazione con lo stesso codice del pacchetto e il codice del prodotto, i due valori possono divergere durante l'aggiornamento dell'applicazione. Per ulteriori informazioni, vedere [codici di pacchetto](package-codes.md).

 

 



