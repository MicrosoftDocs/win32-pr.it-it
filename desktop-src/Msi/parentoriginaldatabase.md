---
description: Durante un'installazione simultanea, il programma di installazione imposta la proprietà ParentOriginalDatabase nella sessione dell'installazione simultanea sullo stesso valore della proprietà OriginalDatabase nella sessione dell'installazione padre.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: ParentOriginalDatabase - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31d022aa4ec7274d464943d8b3ec059ce11142f06e0e09c22bbb42ec40a2e5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913271"
---
# <a name="parentoriginaldatabase-property"></a>ParentOriginalDatabase - proprietà

Durante un'installazione simultanea, il programma di installazione imposta la proprietà **ParentOriginalDatabase** nella sessione dell'installazione simultanea sullo stesso valore della proprietà [**OriginalDatabase**](originaldatabase.md) nella sessione dell'installazione padre. Le installazioni padre usano le azioni di installazione simultanee per eseguire un'installazione simultanea. Un pacchetto di installazione può determinare se viene installato da un'azione di installazione simultanea controllando il valore di questa proprietà.

> [!Note]  
> Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere [Installazioni simultanee.](concurrent-installations.md)

 

> [!Note]  
> Questa proprietà non viene impostata se l'installazione simultanea viene eseguita [dall'azione RemoveExistingProducts.](removeexistingproducts-action.md)

 

## <a name="remarks"></a>Commenti

Per evitare che un pacchetto venga installato come installazione simultanea, aggiungere una delle istruzioni condizionali seguenti alla [tabella LaunchCondition.](launchcondition-table.md) In questo modo si impedisce che il pacchetto venga installato da un'azione di installazione simultanea eseguita da un'altra installazione. Ciò non impedisce l'installazione del pacchetto tramite [l'azione RemoveExistingProducts.](removeexistingproducts-action.md)

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[**ParentProductCode**](parentproductcode.md)
</dt> </dl>

 

 




