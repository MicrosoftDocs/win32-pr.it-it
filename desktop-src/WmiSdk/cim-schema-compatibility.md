---
description: Compatibilità con lo schema CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Compatibilità con lo schema CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df559469ef6a8284b51951dc365bad6c302ca865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316572"
---
# <a name="cim-schema-compatibility"></a>Compatibilità con lo schema CIM

Un componente chiave dell'infrastruttura di Strumentazione gestione Windows (WMI) è un modello orientato a oggetti delle entità gestibili in un sistema. Il modello è conforme a uno standard gestito dal Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) ed è noto come Common Information Model (CIM). Lo schema CIM fornisce un unico meccanismo di descrizione dei dati per tutti i dati forniti.

A partire da Windows 7, WMI è compatibile con la versione dello schema CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ). Gli utenti possono ora compilare uno schema definito da DMTF in un computer Windows.

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a>Vantaggi della compatibilità 2.17.1 della versione dello schema CIM

-   Quando un utente Scarica file MOF 2.17.1 o DMTF MOF, questi ultimi possono essere compilati correttamente nel computer Windows di destinazione.
-   La versione dello schema CIM 2.17.1 ha aggiunto il supporto per BIOS, stampanti, messaggi standard, stato del sistema operativo, paradigmi di risparmio energia moderni, virtualizzazione e sicurezza.
-   La versione dello schema CIM 2.1.7.1 offre supporto del profilo aggiuntivo. Per altre informazioni, vedere attraversamento di [associazioni tra spazi dei nomi](cross-namespace-association-traversal.md)

 

 



