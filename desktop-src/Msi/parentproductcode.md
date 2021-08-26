---
description: Durante un'installazione simultanea, il programma di installazione imposta la proprietà ParentProductCode nella sessione dell'installazione simultanea sullo stesso valore della proprietà ProductCode nella sessione dell'installazione padre.
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: ParentProductCode - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a56e7a120455723eb95f2bd7f5ea08c59894d3a1951aeb042afb30e3b0e2fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042451"
---
# <a name="parentproductcode-property"></a>ParentProductCode - proprietà

Durante un'installazione simultanea, il programma di installazione imposta la proprietà **ParentProductCode** nella sessione dell'installazione simultanea sullo stesso valore della proprietà [**ProductCode**](productcode.md) nella sessione dell'installazione padre. Le installazioni padre eseguono le azioni di installazione simultanee per eseguire un'installazione simultanea. Un pacchetto di installazione può determinare se viene installato da un'azione di installazione simultanea controllando il valore di questa proprietà.

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
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[**ParentOriginalDatabase**](parentoriginaldatabase.md)
</dt> </dl>

 

 




