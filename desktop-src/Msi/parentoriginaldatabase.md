---
description: Durante un'installazione simultanea, il programma di installazione imposta la proprietà ParentOriginalDatabase nella sessione dell'installazione simultanea sullo stesso valore della proprietà OriginalDatabase nella sessione dell'installazione padre.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: Proprietà ParentOriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab69dff7058336a5b68fd3373100f4789059ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329741"
---
# <a name="parentoriginaldatabase-property"></a>Proprietà ParentOriginalDatabase

Durante un'installazione simultanea, il programma di installazione imposta la proprietà **ParentOriginalDatabase** nella sessione dell'installazione simultanea sullo stesso valore della proprietà [**OriginalDatabase**](originaldatabase.md) nella sessione dell'installazione padre. Le installazioni padre utilizzano le azioni di installazione simultanee per eseguire un'installazione simultanea. Un pacchetto di installazione può determinare se viene installato da un'azione di installazione simultanea controllando il valore di questa proprietà.

> [!Note]  
> Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).

 

> [!Note]  
> Questa proprietà non viene impostata se l'installazione simultanea viene eseguita dall'azione [RemoveExistingProducts](removeexistingproducts-action.md) .

 

## <a name="remarks"></a>Commenti

Per impedire l'installazione di un pacchetto come installazione simultanea, aggiungere una delle seguenti istruzioni condizionali alla tabella [LaunchCondition](launchcondition-table.md) . In questo modo si impedisce che il pacchetto venga installato da un'azione di installazione simultanea eseguita da un'altra installazione. Questo non impedisce l'installazione del pacchetto tramite l'azione [RemoveExistingProducts](removeexistingproducts-action.md) .

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[**ParentProductCode**](parentproductcode.md)
</dt> </dl>

 

 




