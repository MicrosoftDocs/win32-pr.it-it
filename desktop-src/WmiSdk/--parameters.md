---
description: Definisce i parametri di input e output per i metodi.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: __PARAMETERS classe
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
ms.openlocfilehash: a2f39cb7b88977c8f61e562badaa6cbda7a5004fc2d0edf70eb59c6276070efd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110566"
---
# <a name="__parameters-class"></a>\_\_Classe PARAMETERS

La **\_ \_ classe di** sistema PARAMETERS è una classe astratta che definisce i parametri di input e output per i metodi. Viene inoltre usato per passare i valori dei parametri di input e output tra un client WMI e un provider di metodi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>Members

La **\_ \_ classe PARAMETERS** non definisce membri.

## <a name="remarks"></a>Commenti

Per definire un metodo in una classe utente, un client WMI crea una copia della **\_ \_ classe PARAMETERS** e aggiunge una proprietà per ogni parametro di input in un metodo. Se il metodo contiene un valore restituito o parametri di output, è necessario creare un'altra copia di **\_ \_ PARAMETERS.** Se il metodo restituisce un valore restituito, il client deve aggiungere una proprietà denominata **ReturnValue**. Il provider di metodi archivia quindi i parametri del metodo con una chiamata a [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Per richiamare un metodo, un client chiama quanto segue in sequenza:

1.  [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) per recuperare una copia della classe **\_ \_ PARAMETERS** archiviata da [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).
2.  [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)e quindi imposta una proprietà per ogni parametro di input sul metodo .
3.  [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) per eseguire il metodo.

Al termine dell'esecuzione del metodo, è possibile che venga restituita un'altra istanza della classe **\_ \_ PARAMETERS** se il metodo ha parametri di output o un valore restituito.

-   Se il metodo è stato richiamato tramite [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), l'istanza **\_ \_ PARAMETERS** viene restituita come argomento di output.
-   Se il metodo è stato richiamato tramite [**IWbemServices::ExecMethodAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)l'istanza **\_ \_ PARAMETERS** viene restituita come parametro a [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).

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

[**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[Chiamata di un metodo](calling-a-method.md)
</dt> </dl>

 

 




