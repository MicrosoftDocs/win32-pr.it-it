---
description: Ottiene i dati non elaborati per una struttura E-EDID (Enhanced Extended Display Identification Data) VESA (Video Electronics Standard Association) specificata che definisce le impostazioni ottimali per la configurazione di un monitoraggio.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Metodo WmiGetMonitorRawEEdidV1Block della classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: dacd0c44a6c0fa8270a65155583f8041616f98674d0798db8b13a72d13751653
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558086"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a>Metodo WmiGetMonitorRawEEdidV1Block della classe WmiMonitorDescriptorMethods

Il metodo **WmiGetMonitorRawEEdidV1Block** ottiene i dati non elaborati per una struttura E-EDID (Enhanced Extended Display Identification Data) VESA (Video Electronics Standard Association) specificata che definisce le impostazioni ottimali per la configurazione di un monitoraggio.

## <a name="syntax"></a>Sintassi


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BlockId* \[ Pollici\]
</dt> <dd>

Identità del blocco di dati.

</dd> <dt>

*BlockType* \[ Cambio\]
</dt> <dd>

Tipo di blocco di dati. Nella tabella seguente sono elencati i valori restituiti possibili.



| Valore                                                                                 | Significato                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Inizializzazione annullata<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Blocco di base EDID<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | Mappa a blocchi EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Altri<br/>           |



 

</dd> <dt>

*BlockContent* \[ Cambio\]
</dt> <dd>

Matrice a 128 byte che contiene il contenuto del blocco non elaborato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per altre informazioni sui codici di errore, vedere [**Costanti di**](/windows/desktop/WmiSdk/wmi-error-constants) errore WMI o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente vengono recuperati i blocchi EDID di qualsiasi visualizzazione come matrici a 128 bit non elaborati.


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

