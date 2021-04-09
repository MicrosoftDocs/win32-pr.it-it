---
description: L'oggetto Microsoft. Windows. ActCtx fa riferimento a manifesti e fornisce un modo per eseguire lo scripting dei motori per accedere agli assembly side-by-side. L'oggetto Microsoft. Windows. ActCtx può essere utilizzato per creare un'istanza di un assembly affiancato con componenti COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Oggetto Microsoft. Windows. ActCtx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880857"
---
# <a name="microsoftwindowsactctx-object"></a>Oggetto Microsoft. Windows. ActCtx

L'oggetto **Microsoft. Windows. ACTCTX** fa riferimento a manifesti e fornisce un modo per eseguire lo scripting dei motori per accedere agli assembly side-by-side. L'oggetto **Microsoft. Windows. ACTCTX** può essere utilizzato per creare un'istanza di un assembly affiancato con componenti com.

L'oggetto **Microsoft. Windows. ACTCTX** viene visualizzato come assembly in Windows Server 2003. Può anche essere installato da applicazioni che usano la Windows Installer per il programma di installazione e lo includono come modulo merge nel pacchetto di installazione.

## <a name="members"></a>Membri

L'oggetto **Microsoft. Windows. ACTCTX** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **Microsoft. Windows. ACTCTX** dispone di questi metodi.



| Metodo                               | Descrizione                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**CreateObject**](createobject.md) | Crea un oggetto nel contesto del manifesto corrente.<br/>            |
| [**GetObject**](getobject.md)       | Ottiene un'istanza di un oggetto **Microsoft. Windows. ACTCTX** esistente.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **Microsoft. Windows. ACTCTX** dispone di queste proprietà.



| Proprietà                                | Tipo di accesso          | Descrizione                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**Manifesto**](manifest.md)<br/> | Sola lettura<br/> | Ottiene il contesto di attivazione attiva.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



 

 




