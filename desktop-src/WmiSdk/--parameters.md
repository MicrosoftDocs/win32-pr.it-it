---
description: Definisce i parametri di input e output per i metodi.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: Classe __PARAMETERS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313217"
---
# <a name="__parameters-class"></a>\_\_Classe PARAMETERS

La classe di sistema **\_ \_ Parameters** è una classe astratta che definisce i parametri di input e output per i metodi. Viene inoltre utilizzato per passare i valori dei parametri di input e di output tra un client WMI e un provider di metodi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>Members

La classe **\_ \_ Parameters** non definisce membri.

## <a name="remarks"></a>Commenti

Per definire un metodo in una classe User, un client WMI crea una copia della classe **\_ \_ Parameters** e aggiunge una proprietà per ogni parametro di input in un metodo. Se il metodo contiene un valore restituito o parametri di output, è necessario creare un'altra copia dei **\_ \_ parametri** . Se il metodo restituisce un valore restituito, il client deve aggiungere una proprietà denominata **returnValue**. Il provider di metodi archivia quindi i parametri del metodo con una chiamata a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Per richiamare un metodo, un client chiama quanto segue in sequenza:

1.  [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) per recuperare una copia della classe **\_ \_ Parameters** archiviata da [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).
2.  [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), quindi imposta una proprietà per ogni parametro di input per il metodo.
3.  [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) per eseguire il metodo.

Al termine dell'esecuzione del metodo, è possibile che venga restituita un'altra istanza della classe di **\_ \_ parametri** se il metodo ha parametri di output o un valore restituito.

-   Se il metodo è stato richiamato usando [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), l'istanza di **\_ \_ Parameters** viene restituita come argomento di output.
-   Se il metodo è stato richiamato usando [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), l'istanza di **\_ \_ Parameters** viene restituita come parametro a [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> </dl>

 

 




